---
description: Blog updates for my work at IBM HDC
icon: display-code
---

# IBM HDC

## KubeRay Experiments [WIP]

Add experience running RayCluster job on Luigi's hugging face code

- Was running this [KubeRay job example](https://docs.ray.io/en/latest/cluster/kubernetes/examples/mnist-training-example.html#kuberay-mnist-training-example) on PDG cluster and ran into some issues with resource allocation.

- I got an error that the /tmp was overspilling. I looked up online and it said I can mount a volume to the pods so that ray writes to the volume instead. I have done something similar when running on GPU VM. I noticed though Luigi was able to run the cluster in his repo by giving a higher memory allocation in the yaml (increased memory of worker nodes from 4 - 24 GiB) and thought it should be worth the first try instead. I tried that and it worked. I am running the job now and it seems to be going smoothly though slow. I think there are 10 epochs with each epoch taking about 5 minutes. 

![alt text](assets/images/IBM-HDC/image.png)



- Now my next course of action was to modify, the previous extractor I wrote in clowder, which helps train foundation models using Hugging Face transformers for a specific task, into a RayCluster job. 

- The job previously ran on a GPU environment but the aim is to get near similar speeds with KubeRay. I will first start with a specific script before moving to using Clowder Extractor to provide the input, output and starting the job

- Notes while writing new script:
    - Using the new TorchTrainer API (`Ray 2.7 introduced the newly unified TorchTrainer API, which offers enhanced transparency, flexibility, and simplicity. This API aligns more with standard Hugging Face Transformers scripts, ensuring that you have better control over your native Transformers training code.`). 
    - The script is using Ray Datasets to load the data. 
    - The script has more specificity when it comes to workers and batch_sizes
    
- Notes while deploying to K8:
    - I ran into some issues with enviornment and coding errors
    - I set max_steps for training which was necessary but that overwrites num_train_epochs
    `
    35[36m(RayTrainWorker pid=502, ip=10.42.0.7)[0m max_steps is given, it will override any value given in num_train_epochs
    36
    ` 

    - I switched to a more basic script and it started working but stopped the job and switched to a different bert model cos the original is too large to train
    - Getting a lot of errorswith tensor length on replacing