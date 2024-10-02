---
description: Blog updates for my work at IBM HDC
icon: display-code
---

# IBM HDC

## KubeRay Experiments

### 1. Introduction to Kubernetes and Ray
I began by familiarizing myself with Kubernetes and Ray, focusing on running Luigi's Clowder extractors for image classification on a Ray Cluster deployed on Kubernetes. The extractors utilized the Ray Job API to submit tasks to the cluster. After minor adjustments, the extractors ran successfully on the cluster.

### 2. Shift to Training Jobs on Ray Cluster
The project shifted towards training models on the Kubernetes cluster. Since our K8s cluster lacks GPUs, I followed CPU-based examples from the Ray documentation. I ran the [KubeRay MNIST training job](https://docs.ray.io/en/latest/cluster/kubernetes/examples/mnist-training-example.html#kuberay-mnist-training-example) on the PDG cluster but encountered resource allocation issues.

An error occurred due to the `/tmp` directory overspilling. While one solution was to mount a volume to the pods, I first attempted increasing the memory allocation of worker nodes from 4 GiB to 24 GiB, similar to Luigi's setup. This adjustment resolved the issue, and the job ran successfully, albeit slowly, with each epoch taking around 5 minutes (10 epochs in total).

![RayJob Output](assets/images/IBM-HDC/image.png)

### 3. Modifying Existing Training Extractor for Ray Cluster

I proceeded to modify the previous Clowder extractor, which was designed to train foundation models using Hugging Face transformers, into a RayCluster job. The original job ran on a GPU environment, but the goal is to achieve comparable speeds using KubeRay.

As a side note, I tried improving the script's performance by using Ray Datasets to load the data. The script also had more specificity regarding workers and batch sizes. However, I encountered issues I was unable to resolve so thought I pivot to a more basic script and come back to this later.

- **Deployment on K8s**: During deployment, I encountered several issues:
    - Environment and coding errors arose early on.
    - I got it working with the BERT model but that was taking a long time for just a small sample of the data

    ![BERT model training log](assets/images/IBM-HDC/image-2.png)

    -**Switch to a Smaller Model:** I switched to using [Tiny-Bert](huggingface.co/prajjwal1/bert-tiny) to reduce the timing issue, however ran into some issues with input dimensions. The fix was to set the `max_length` parameter and use padding to ensure the input tensor lengths matched. 
    
    - **Storage Issues:** I encountered storage issues and realized we needed a shared storage resource for the worker nodes. I created a Taiga mounted PVC and mounted it to the worker nodes, which resolved the issue. 

    ![Ray Doc Excerpt](assets/images/IBM-HDC/image-3.png)

The model was then able to train successfully though the accuracy was low due to the small dataset size, the model's simplicity.

![Simple Bert Model Trained](assets/images/IBM-HDC/image-1.png)


### Takeaways and next steps:

- I am currently using a RayJob, but when using extractors we will need to submit jobs to a RayCluster. Luigi has already done something similar on the inference extractor so this should be an easy transition.

- Working on this script, I realized we need to give users control over more minute configuration details such as tokenization parameters. It does not need to be resolved now but it is something to keep in mind.

- The exporting of the best model from this cluster back to Clowder (is probably straightforward using the Clowder API)  

- Need to see how it handles pod failures

- How easily can the script be ported to a GPU environment?

- **Autoscaling** - Dynamic resource allocation based on the load for large datasets and models

- **Model Versioning** - Implementing a versioning system for models to track changes and improvements. Can users pick the best model from the cluster and export it back to Clowder?


