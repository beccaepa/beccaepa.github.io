---
# Always set this as 'post'.
layout: post

# Set the title of the blog here
title:  "Unsupervised Question Decomposition for Questions Answering"

# Set the date here, format must be YYYY-MM-DD hh:mm:ss +TTTT.
date: 2020-03-31 00:00:00 +0000

# Set the path of the image file, example /assets/images/blog/image.jpg
# You can also use an online URL as well, example https://www.google.com/image.jpg
# Image is optional, if not provided no image will be shown.
image: /assets/images/unsupervised_image1.png

# This is an optional field which sets the link of the blog post.
# If not provided, a link will be generated automatically with the title of the blog post.
permalink: blog/unsupervised-decomposition/

# This is the excerpt of the blog post which will be shown in the blog listing page.
excerpt: We improve question answering (QA) by decomposing hard questions into easier sub-questions that existing QA systems can answer. 
---

<!-- Add the blog post here in markdown -->

We improve question answering (QA) by decomposing hard questions into easier sub-questions that existing QA systems can answer. Since annotating questions with sub-questions is time-consuming, we propose an unsupervised approach to produce sub-questions, which also lets us learn from millions of questions from the Internet. We answer sub-questions with an off-the-shelf QA model and incorporate the resulting answers in a downstream QA system, showing strong improvements on multi-hop QA.

![Inverse Scaling Prize Ideas](/assets/images/unsupervised_image1.png)

## **How it works:**

To train the decomposition model, we construct a noisy, “pseudo-decomposition” for each hard question by retrieving similar, simple questions from a large corpus. We then train neural text generation models on that data with standard sequence-to-sequence learning or unsupervised sequence-to-sequence learning, as shown below.

![Inverse Scaling Prize Ideas](/assets/images/unsupervised_image2.png)

Our approach automatically learns to generate useful decompositions for many types of questions, highlighting the general nature of our approach. Question decompositions also add a form of interpretability to black-box, neural QA models; we can see what sub-questions and answers the model used to make its prediction, as shown below:

![Inverse Scaling Prize Ideas](/assets/images/unsupervised_image4.png)

## **Why it matters:**

In machine learning, we often train models to solve new kinds of examples from scratch. Our approach shows a way to leverage the abilities of existing models in order to tackle new examples, improving generalization to new examples without requiring manual annotation.

## **Get it on GitHub:**

Code: [https://github.com/facebookresearch/UnsupervisedDecomposition](https://github.com/facebookresearch/UnsupervisedDecomposition)

Paper: [https://arxiv.org/abs/2002.09758](https://arxiv.org/abs/2002.09758)
