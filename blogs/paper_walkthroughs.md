---
description: Notes on Papers 
icon: display-code
---

# Paper Walkthroughs

## [How to Present a Paper in Theoretical Computer Science](https://ianparberry.com/pubs/speaker.pdf)

In my work, there is a lot of communication with stakeholders and peers, where I walk them through my work. To improve my presentations, I read this paper to get some guidance even if the paper is about presenting papers. I will jot down the key points which pertain to my needs.

### What to say and how to say it?

While selecting the material to present, the author suggests keep the following in mind:

- **Commuicate the Key Ideas**

    New results = few key ideas + application of standard tools and techniques. Emphasize the key ideas and not the details.

- **Dont get bogged down in details**

    Dont alienate the audience, launching right into the technical details. Start with a high-level overview and then delve into the details. Motivate the audience to listen to the details.

- **Structure your talk**

    The presentation should be broken into several distinct parts, each with it's own objectives and style. The audience should be steered gently from one part to the next.

- **Use a Top-down Approach**

    Template for talk consists of 4 parts:
    1. **Introduction**: General overview of the presentation
    2. **The Body**: Detailed explanation but abstract.
    3. **The Technicalities**: Detailed explanation of the technical details.
    4. **Conclusion**: Summary of the results and future work.

    This template needs to be modified specifically points 2 and 3 based on the subject matter. For example, very technically complex presentations may require more than one pass in the body.


### Breaking down the parts

- **Introduction**

    The most important part. It sets the tone and a lot of snap decisions are made based on the introduction. 
    
    - **Define the problem** - Take time to explain the problem and why it is important. Else the audience will not be interested or understand the rest of the talk.

    - **Motivate the Audience** - Explain why the problem is interesting. *Throw in a little philosophy if necessary*, how can it fit into the larger picture. Other questions:
        - What are its applications?
        What makes the problem nontrivial
    These questions can then be revisited in the conclustion to see how we address them

    - **Introduce Terminology**- Keep to minimum but it will be impossible to completely avoid.

    - **Discuss Earlier Work** 

    - **Provide a Road-map** - Give the audience a brief guide to the rest of the talk as the last paragraph of the introduction. *But don’t make it a dry litany of dull generalizations (“first I will present the introduction, then summarize earlier work, then present the main body, and end with the conclusion”). Instead, give a short preview of what will be in each section. This part of the talk can be eliminated for very short conference presentations.*

- **The Body**

    - **Abstract the Major Results** - Do not get too technical, keep it as abstract and describe the key results.

    - **Explain the significance of the results** - Why are the results important? How do they fit into the larger picture?

**Getting Technical**

Give some technical details for those who are proficient in the field. Present it carefully, be succint nad clear. Aim for understanding over content. 

**The Conclusion**

**Hindsigh is clearer that foresight** - Present the observations that would have been confusing to present till now.  Refer to previous info and make a coherent synopsis.

**Give open problems** - Mention shortcomings and open problems. This is a good way to show that you are aware of the limitations of your work. 

- **Indicate end of talk** - LOL (Seriously, this is what the paper says). Say Thank you, are there any questions and then end the talk. 

###Z Getting Through to the Audience

- **Use Repetition**  
  Oral presentations should follow the pattern:  
  - Introduction: Tell them what you're going to tell them.  
  - Body/Technicalities: Tell them.  
  - Conclusion: Tell them what you told them.  
  Repetition helps clarify misunderstandings by rephrasing information in different ways.

- **Remind, Don’t Assume**  
  Briefly remind the audience of "standard" results in your field, even if they are widely known. Phrasing it as a reminder, allows those unfamiliar to learn without feeling embarrassed and those familiar to tune out if needed.

- **Don’t Over-run**  
  Avoid exceeding the allotted time. Plan to finish 5 minutes early to leave time for questions. Quality tends to decrease as the talk over-runs. Rehearse to ensure your talk fits within the given time. If short on time, cut out the technical details.

- **Maintain Eye Contact**  
  Spread your attention throughout the audience, and glance at the session chair periodically for time cues.

- **Control Your Voice**  
  Speak clearly, at an appropriate volume, and avoid monotony. Avoid filler words and hype.

- **Control Your Motion**  
  Project energy with natural gestures. Avoid being rooted in one spot or excessive movement, and be mindful of your position relative to the projector screen or dais.

- **Take Care with Your Appearance**  
  Dress appropriately for the occasion. For job talks, formal attire is recommended. For colloquia or conferences, casual attire is acceptable.

- **Minimize Language Difficulties**  
  If speaking in a non-native language, focus on clear delivery. Have a native speaker review your slides. Avoid reading from a prepared text.

- **Try Not to Get Anxious**  
  Preparation and practice reduce anxiety. Ignore distracting reactions from the audience. If you feel panicked, pause, breathe, and then continue. Mistakes in early talks are not career-ending.

## Handling Questions at the End of a Presentation

- **Three Types of Questions**
  1. **Genuine Requests for Knowledge**  
     These are straightforward and can be handled easily with adequate preparation.
  
  2. **Selfish Questions**  
     These are designed to bring attention to the questioner. Take a few seconds to craft a thoughtful reply that subtly compliments them.

  3. **Malicious Questions**  
     These aim to undermine you, possibly as a test of handling criticism or out of insecurity. Expect attacks on your topic selection, proofs, or references. Stay polite, avoid prolonged exchanges, and offer to discuss offline if needed.

- **Saying "I Don’t Know"**  
  It's okay to admit if you don't know the answer. Deliver this with confidence, and avoid confusing "I don’t know" with "it is not known" unless you're sure. Follow up with the questioner later to learn more if possible.

Also read [How to give a technical presentation](https://homes.cs.washington.edu/~mernst/advice/giving-talk.html)

## [How to Read a Paper](http://ccr.sigcomm.org/online/files/p83-keshavA.pdf)

Given I am going to fill this page with short notes on the papers I read, I think the first step is to learn how to read a paper. This paper provides a systematic way to read a paper.

### The Three-Pass Approach 

The idea is to go through the paper thrice, each time with a specific goal in mind. The first pass is to get a general idea about the paper. The second pass is to grasp the conent but not the details. The third pass is to understand the paper in depth.

**First Pass**

The pass should take 5 to 10 minutes. Consists the following steps:

- Carefully read the title, abstract and introduction.
- Read the section and sub-section headings.
- Read the conclusions.
- Glance at the references.

You should be able to answer the following questions after the first pass (the 5 Cs):
1. Category: What type of paper is this? A measure- ment paper? An analysis of an existing system? A description of a research prototype?
2. Context: Which other papers is it related to? Which theoretical bases were used to analyze the problem?
3. Correctness: Do the assumptions appear to be valid?
4. Contributions: What are the paper’s main contribu-
tions?
5. Clarity: Is the paper well written?

This can help us decide whether to read the paper in detail. In case, it doesnt interest us or know enough about the area of research. 

**Second Pass**


Read with greater care but ignore details like proof. Jot down key points or make comments.

1. Loook carefully at illustrations
2. Mark relevant unread references

This can take up to an hour. We should be able to summarize the main thrust of the paper to someone else. 
It is possible to not under understand the paper because of complexity or subject matter. You can:

- Set the paper aside, hoping you dont need to unserstand the material
- Retyrn to paper later, after reading background material
- Go to the third pass



**Third Pass**

I think this is optional. It is to understand the paper in depth or if you are a reviewer. The key is to *virtually re-implement* the paper.

To quote the paper:

*This pass requires great attention to detail. You should identify and challenge every assumption in every statement. Moreover, you should think about how you yourself would present a particular idea. This comparison of the actual with the virtual lends a sharp insight into the proof and presentation techniques in the paper and you can very likely add this to your repertoire of tools. During this pass, you should also jot down ideas for future work.*

The pass can take 4-5 hours for novices. This is basically learning the paper by heart. 

### A Literature Survey

I dont need to do a literature survey but the steps are useful for me to find papers. 

There are so many papers. the author suggests the following steps:

1. First, use an academic search engine such as Google Scholar or CiteSeer and some well-chosen keywords to find three to five recent papers in the area. Dp a one pass on each paper to decide which one to read in detail.

2. Find shared citations. This is a good way to find seminal papers in the area.

3. Gp to the website for these top conferences and look through their recent proceedings. A quick scan will usually identify recent high-quality related work.