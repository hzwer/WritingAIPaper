# Writing AI Conference Papers: A Handbook for Beginners

Crafting a research manuscript can pose significant challenges for novices, particularly when time is scarce before the deadline and the authors lack experience in academic submissions. An ill-prepared manuscript can be a source of distress for both collaborators and readers, frequently leading to rejection or necessitating substantial revisions. In this article, we'll share some tips for beginners who want to write AI conference papers. Our goal is for this article to be a guide for beginners, making it easier to share academic achievements.

[PDF version](https://drive.google.com/file/d/1hbQ8qvVPUndNRSwK2Hq6wLwh8sxapi95/view?usp=sharing)

## Introduction

The GPU cluster has been running for half a year, and you feel that the results are already significant. You realize that the deadline for an upcoming conference is less than a month away, yet you have only written some course assignment reports. How far in advance should the first draft be completed to avoid missing the deadline? What distinguishes a good research paper from a bad one? What should be done before starting to write? These questions plague you like a nightmare, leaving you staring at the blank Overleaf homepage. Luckily, this article is written for you. Having experienced the agony of rejection and the joy of acceptance, we hope to provide some insights for novices.

In this article, we will discuss the aspects related to writing conference papers, with a focus on common pitfalls, catering to novices. Our article mainly consists of two parts: completing a paper and refining its details. We aim to provide practical guidance that will enable novices to navigate the complexities of academic writing and contribute to the field with clarity and confidence. Sincerely, we recommend the [Resource List of Writing Tips](https://vision.sjtu.edu.cn/writing.html) curated by Professor Chao Ma.

## Build A Paper From Scratch

This section outlines writing an AI paper from scratch, covering structure, core idea, framework, results, and introduction.

### The Hierarchical Structure
***Take-away: Abstract - Introduction - Main body, which are gradually unfolded. Each part is self-complete.***

The typical structure of a paper includes 1. an abstract, 2. an introduction, and 3. the main body, which encompasses sections such as related work, methodology, experiments, discussion, conclusion, and references. We can break down this structure into three levels. At each level, you should aim to convey a comprehensive research narrative. Each level serves as an expansion of the preceding one. With this understanding, let's explore how to effectively present a research story. For those who are starting out, it's advisable to focus on completing the main body of the paper first.

### Find the Core Idea
You may have interesting findings and experimental results, but you're unsure how to define the core theme. \textit{The key contribution of most published papers falls into exactly one out of the following three categories~\cite{nowozin2015ten}:}

*Insight: you have an explanation for something that is already there.*

*Performance: you can do something better.*

*Capability: you can do something that could not be done before.*

Identify the core advantages of your work and emphasize them early in your paper. You can further expand the overall \textbf{novelty} from other aspects as well. Key research topics, efficient solutions, and innovative technical contributions are the primary elements that contribute to a paper's novelty. For instance, numerous early influential works of deep learning emerged from foundational model research due to their potential to impact the entire field. Techniques such as "Batch Normalization"~\cite{ioffe2015batch} and "Residual Learning"~\cite{he2016deep} are esteemed for their effectiveness.   By emphasizing the novelty of your work, you'll be able to discern which aspects are worth the effort and which are inconsequential details.

*We suggest a short article titled [Novelty in Science](https://medium.com/@black_51980/novelty-in-science-8f1fd1a0a143).*

***Take-away: Clearly describe the increment over previous methods and find one or two core ideas.***

Readers seek novel insights when reading papers. A good paper should have strong points that are easy to remember. Refine your central ideas until you're confident that people will be eager to learn about them and share them widely. It should be noted in particular that some ideas may be great, but if they lack originality, it is not advisable to describe them in detail in the paper.

Don't underestimate the novelty of your own work. Delve deep to uncover the underlying principles. If the ResNet paper were rewritten as: "We designed a model using a large number of $3\times3$ convolutions (inspired by VGGNet) and parallel shortcuts (simplified from GoogleNet) **based on** the former two", then it will also become a paper without novelty. The line of ResNet is to propose a problem, abstract the underlying principles, propose its own solutions and specific implementations, and verify them experimentally. This might not totally reflect their research process, but it effectively showcases their discoveries.

### Construct the Framework
***Take-away: Consider the target audience, introduce the valuable findings rather than the tortuous research process.***

While adhering to the core ideas, start outlining the content you intend to present in your paper. Begin by creating a simple slide to demonstrate your research approach and achievements to your peers, colleagues, or mentors, in order to assess their understanding. It may be beneficial to intentionally seek feedback from researchers unfamiliar with your work to identify potential gaps in comprehension. Unlike the experimental process, it is advisable to emphasize valuable novelties and avoid presenting incomplete or complex aspects of your research. Continuously review and refine your presentation from the reader's perspective until it is easily understandable.

It may also be necessary to supplement your work with additional experiments if you feel that your experimental rationale lacks rigor. At the same time, it is advisable to conduct thorough literature research, ideally identifying several papers with highly relevant topics. Consider these as potential competitors to your paper and examine them for areas of improvement. Reflect on which aspects would captivate the community and accentuate them, while minimizing the inclusion of clichéd content. 

### Make the Results More Solid
***Take-away: Around the contribution statements, conduct a solid analysis in result section.***

Many readers will initially assess the method's effectiveness by examining the results before deciding to read the entire paper. They'll look to see if your contribution aligns with the experimental findings. Even with strong confidence in your method's efficacy, you'll likely need additional comparative and ablation experiments. It's important to create more tables and visuals, selecting the most significant aspects to present. Honesty and objectivity are crucial; overstating claims is particularly undesirable. If concerned about overclaiming, discussing with peers is advisable.

### Write An Introduction
Regarding the structure of the introduction, we directly quote from the textbook~\cite{swales2004academic,kallestinova2011write}:

**Move 1. Establish a research territory**

a. Show that the general research area is important, central, interesting, and problematic in some way;

**Move 2. Find a niche**

a. Indicate a gap in the previous research, or extend previous knowledge in some way.

**Move 3. Occupy the niche**

a. Outline purposes or state the nature of the present research;

b. List research questions or hypotheses;

c. Announce principle findings;

d. State the value of the present research;

e. Indicate the structure of the research paper.

**Additional suggestions:**

a. Cut to the chase and don't write too much irrelevant to the paper's topic;

b. Respect the work of predecessors, and affirm historical contributions before pointing out shortcomings;

c. Knuth: *Keep the reader upper-most in your mind.*

d. Consider using a "page one figure" to highlight the most important aspects of the paper and catch the reader's attention.
