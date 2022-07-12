---
layout: post
title: Image Aesthetics Assessment with AI
subtitle: Learn and discuss the image aesthetics assessment problem and artificial intelligence based solutions for it.
background: /img/academic/iaa/background.jpg
tags: Academic
comments: true
permalink: /image-aesthetics-assessment-with-ai.html
---

> TL;DR: Learn and discuss the image aesthetics assessment problem and artificial intelligence based solutions for it.
> Liên kết đến bản tiếng Việt của bài viết có thể được tìm thấy tại [đây](https://hieuphung97.com/danh-gia-tham-my-anh-cung-tri-tue-nhan-tao.html).

---

#### Table of Contents
- [Introduction](#intro)
- [Why is Image Aesthetics Assessment Important?](#why-iaa)
- [How do We Assess Image Aesthetics?](#how-iaa)
- [**Image Aesthetics Assessment with AI**](#iaa-with-ai) 👈
- [Discussion](#discussion)
- [References](#references)

<br/>

---

#### Should have background knowledge
<ul>
  <li><a href="https://en.wikipedia.org/wiki/Machine_learning" target="_blank">Machine learning</a>
    <ul>
      <li><a href="https://en.wikipedia.org/wiki/Statistical_classification" target="_blank">Classification problem</a></li>
      <li><a href="https://en.wikipedia.org/wiki/Regression_analysis" target="_blank">Regression problem</a></li>
      <li><a href="https://en.wikipedia.org/wiki/Ranking" target="_blank">Ranking problem</a></li>
      <li><a href="https://en.wikipedia.org/wiki/Deep_learning" target="_blank">Deep learning</a></li>
    </ul>
  </li>
</ul>

<hr style="border:1px solid gray">

<br/>

# <a id="intro"></a>Introduction

Aesthetics [[1](#ref-1),[2](#ref-2),[3](#ref-3)] (noun) is the formal study of art, especially in relation to the idea of beauty.

Image aesthetics assessment (IAA) [[3](#ref-3),[4](#ref-4)], when being referred as a problem solved by the machines, is a computer vision problem that aims at categorizing images into different levels of aesthetic; i.e., is making decisions about image aesthetics similar to those of humans.

#### Related terms
- Image quality assessment
- Image memorability
- Image cropping

<br/>

---

# <a id="why-iaa"></a>Why is Image Aesthetics Assessment Important?
Have you ever questioned yourself that have I ever tried to judge the aesthetic of a photo? I bet most of you reading this blog are already doing this, even daily. It doesn't have to be something fancy, the act of assessing image aesthetics occurs during the process of taking this photo. You can adjust the shooting angle, adjust the light, change the aperture of the lens, or ask the model to change her pose,... all to get the best picture of your desire.

Besides spiritual value, beautiful photos could bring great material value as well. That is why we have experts in judging photos' quality. That is why we have image-based social networks like <a href="https://www.instagram.com/" target="_blank">Instagram</a> and <a href="https://www.pinterest.com/" target="_blank">Pinterest</a>. That is why we have <a href="https://en.wikipedia.org/wiki/Stock_photography" target="_blank">stock photography</a> market; e.g., <a href="https://www.pixtastock.com/" target="_blank">Pixtastock</a> in Japan, and the big guy <a href="https://www.shutterstock.com/" target="_blank">Shutterstock</a>, just to name a few.

Another reason, in my opinion, that makes this problem important is that the need of finding beautiful photos on the Internet will increase day by day. As the number of shared photos grows larger and larger, it can become more difficult to find an eye-catching photo. Perhaps, in the near future, sorting photos according to aesthetic scale will become the standard feature of all search engines.

<br/>

---

# <a id="how-iaa"></a>How do We Assess Image Aesthetics?

Now we will see how humans and machines do the job of assessing the aesthetic of photos.

## Humans
As a human, surely each person will have his or her own assessment of image aesthetics; however, to evaluate systematically, we will need to define aesthetic criteria.

For example:
- Composition
- Lighting
- Object emphasis
- The beauty of model
- The beauty of pattern
- Uniqueness of content
- ...

In terms of composition criteria, there are many ways to layout an image, the most popular is probably <a href="https://en.wikipedia.org/wiki/Rule_of_thirds" target="_blank">rule of thirds</a>, then possibly <a href="https://en.wikipedia.org/wiki/Symmetry" target="_blank">symmetry</a>,..., and many others.

<center><img src="/img/academic/iaa/rule_of_thirds.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

Satisfying certain compositional criteria can make a photo looks better. This short video --- <a href="https://www.instagram.com/reel/CaPxY2pqOH0/" target="_blank">instagram.com/reel/CaPxY2pqOH0/</a> shared by <a href="https://www.instagram.com/mitchleeuwe/" target="_blank">mitchleeuwe</a> --- can help you better understand this aesthetic criterion.

<br/>

Regarding the lighting factor, a photo with good lighting can be defined as one with sufficient light, without underexposure or overexposure.

<table>
  <tr>
    <td><center><img src="/img/academic/iaa/lighting.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/lighting_2.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/lighting_3.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
  </tr>
</table>

<br/>

<a href="https://thevirtualinstructor.com/blog/emphasis-a-principle-of-art" target="_blank">Emphasizing</a> the main subject can also make a photo more beautiful. By manipulating elements such as contrast, isolation, convergence, etc., artists can direct the viewer's eyes to certain locations on the image to serve their artistic intent.

<center><img src="/img/academic/iaa/object_emphasis.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

<br/>

The assessment of the attractiveness of models and textures is more subjective, mostly coming from the personal point of view of the reviewer.

<table>
  <tr>
    <td><center><img src="/img/academic/iaa/sailor_moon.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/sailor_moon_2.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
  </tr>
</table>

Depending on one's experience, gender, nationality, religion, etc., each person's assessment of image aesthetics can be different.

<table>
  <tr>
    <td><center><img src="/img/academic/iaa/xo_pattern.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
    <td><center><img src="/img/academic/iaa/memphis_style_pattern.jpg" alt="" title="" style="max-width: 90%; height: auto;"/></center></td>
  </tr>
</table>

<br/>

The uniqueness of the image content even needs the judgment of experts, to choose the photo with the most unique content.

<center><img src="/img/academic/iaa/content_uniqueness.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

And there are many other criteria that we can define to assess the aesthetics of photos. It can be seen that this is not an easy task for humans, there are many factors that can be taken into consideration. So, can machines do this job for us?

## Machines
Before answering the question of whether a machine can assess the aesthetics of images, we will classify the aesthetic criteria listed above into two groups:

- Technical-related criteria
  - Composition
  - Lighting
  - Object emphasis
- Content-related criteria
  - The beauty of model
  - The beauty of pattern
  - Uniqueness of content

The word "technical" has shown the mechanicalness of the criteria belonging to the first group. When humans can evaluate a criterion quantitatively, the decisions made will be more objective and will be more painless for us to teach the machine to know how well an aesthetic criterion is satisfied for each input image.

In contrast, the evaluation criteria related to the content of the image contain many subjective opinions. Finding the rule, therefore, becomes more difficult, more difficult to evaluate mechanically.

In the next section, we will see how researchers address this issue with machines. For now, we know that in order to fully assess the aesthetics of an image, we will need to consider both objective and subjective factors. This poses challenges for humans in transferring this knowledge to the machine in order to simulate the process of assessing image aesthetics.

<br/>

---

# <a id="iaa-with-ai"></a>Image Aesthetics Assessment with AI

<center><img src="/img/academic/iaa/iaa_dimensions.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>
<center><i>Five aspects of IAA problem [<a href="#ref-3">3</a>]</i></center>

The figure above gives us the big picture of the IAA. Five aspects that make up this picture include
- input,
- scope,
- features,
- output,
- and application.

In this blog post, we will focus on only three of them: Feature, output, and scope.

## Features
First of all, talking about the features used for solving the problem, if we consider the solution used to solve the IAA problem as a mill, then we must provide materials to let this mill do its job, and the materials here will be the features. In the studies so far on the problem of assessing image aesthetics, the materials could be...

### Hand-crafted features
With the comprehensive knowledge of photography, physics, mathematics, and possibly many other fields, the experts suggest the features they think might represent the images. For instance, by analyzing the <a href="https://en.wikipedia.org/wiki/Color_histogram" target="_blank">color histogram<a> of photos, perhaps we can find the rules to distinguish an image with harmonious colors from other ones.

<center><img src="/img/academic/iaa/hand_crafted_features.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

Works that use hand-crafted features are often quite old, and the results obtained by the solutions proposed by these works are not really good. However, it is easy to identify the factors that lead to the decisions regarding image aesthetics when using these features.

### Generic features
These are features extracted from images that are not intended to solve a specific problem; e.g., Bag of Visual Words [[5]](#ref-5), Fisher Vectors [[6]](#ref-6), etc. By achieving better results than the old approaches, the solutions use general features has demonstrated that the aesthetic features of the image are implicitly embeded in the general features. This brings us closer to the era of features learned directly from the data --- features learned by deep learning models, or deep features for short.

### Deep features
Features learned directly from data by deep learning models do not require prior knowledge of IAA. The deep learning model will automatically learn the rules from the input data, images in this case, and the corresponding label, or we can say the answer, prepared by the human. The advantage of this method is that it gives much better results than using hand-crafted features. However, one must use a huge amount of data for this method to work, and it will be almost impossible to explain the decisions that a deep learning model makes when assessing the aesthetics of an image.

A few popular deep learning models that are frequently used in recent works about IAA include: AlexNet [[7]](#ref-7), VGG [[8]](#ref-8), MobileNet [[9](#ref-9),[10](#ref-10),[11](#ref-11)], ResNet [[12]](#ref-12).

## Output
Once we provide the mill with materials, we definitely want it to output something for us. The output types of the IAA problem can be divided into four groups, corresponding to four problems: Classification, regression, ranking, and explanation.

### Classification problem
For the classification problem, we can expect the solution to classify an image into different aesthetic levels, low/high aesthetic quality (<a href="https://en.wikipedia.org/wiki/Binary_classification" target="_blank">binary classification</a>), or aesthetic points within a given range (<a href="https://en.wikipedia.org/wiki/Multiclass_classification" target="_blank">multi-class classification</a>). The commonly used metrics to evaluate this problem are those you might already be familiar with, such as <a href="https://en.wikipedia.org/wiki/Accuracy_and_precision" target="_blank">accuracy</a>, <a href="https://en.wikipedia.org/wiki/F-score" target="_blank">F1 score</a>, etc.

<center><img src="/img/academic/iaa/classification_problem.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

### Regression problem
Talk about the regression problem, an image can be graded aesthetically in the form of a real number. Common metrics used for this problem include <a href="https://en.wikipedia.org/wiki/Mean_squared_error" target="_blank">mean squared error (MSE)</a>, <a href="https://en.wikipedia.org/wiki/Mean_absolute_error" target="_blank">mean absolute error (MAE)</a>, etc.

<center><img src="/img/academic/iaa/regression_problem.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

### Ranking problem
For the ranking problem, the popular architecture is Siamese network (architecture of two networks with shared weights) [[13]](#ref-13) combined with a <a href="https://gombru.github.io/2019/04/03/ranking_loss/" target="_blank">loss function for the ranking problem</a>. In addition, we also have Triplet Network [[14]](#ref-14) (architecture of three networks with shared weights) combined with Triplet Loss [[14]](#ref-14). <a href="https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient" target="_blank">Spearman's rank correlation coefficient</a> is the commonly used measurement in this problem.

<center><img src="/img/academic/iaa/ranking_problem.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>

### Prediction explanation problem
Moreover, there is a group of works focused on explaining the aesthetic decisions made by machine learning models. For solutions based on <a href="https://cs231n.github.io/convolutional-networks/" target="_blank">convolutional neural networks</a>, techniques such as CAM [[15]](#ref-15), GradCAM [[16]](#ref-16) are used. The problem of explaining the aesthetic decisions can also exist in the form of a <a href="https://en.wikipedia.org/wiki/Multi-task_learning" target="_blank">multi-task learning</a> problem to evaluate the aesthetic level of an image on multiple aesthetic criteria simultaneously [[17]](#ref- 17), or in the form of an <a href="https://paperswithcode.com/task/image-captioning" target="_blank">image captioning</a> problem to generate text fragments used to explain aesthetic decisions made by the solution [[18]](#ref-18).

## Scope
As mentioned in the above sections, the process of assessing the image aesthetics of humans always holds both objective and subjective factors.

The usual practice to prepare labels for the IAA problem is to score each image multiple times with the participation of numerous individuals. In this way, the aesthetics of an image will be represented by a distribution of scores.

<center><img src="/img/academic/iaa/image_subjectivity.jpg" alt="" title="" style="max-width: 95%; height: auto;"/></center>
<center><i>The subjectivity in scoring image aesthetics [<a href="#ref-3">3</a>]</i></center>

Considering the scope of the IAA problem, there are two approaches.

### Generic approach
Works following this approach consider aesthetics as an inherent attribute of photos, independent of any individual's eyes. Therefore, for each input image, there will be only one corresponding output that reflects the aesthetic of that image. To obtain data for model training, the simplest way is to use the expected value, or simply the mean, calculated from the distribution of the aesthetic score of each image. 

Some works design their solutions that even directly learn the aesthetic score distributions instead of just learning the expected values. Calculating the error between the model's prediction results and the labels will require tools to compute the distance between the probability distributions, such as <a href="https://en.wikipedia.org/wiki/Earth_mover%27s_distance" target="_blank">Earth mover's distance (EMD)</a>, <a href="https://stats.stackexchange.com/a/274861" target="_blank">Chi-square distance</a>, <a href="https://en.wikipedia.org/wiki/Kullback%E2%80%93Leibler_divergence" target="_blank">KL divergence</a>, etc. Typical for this design, we can mention NIMA [[19]](#ref-19). Although it is not the first work to use EMD to learn aesthetic score distribution, NIMA is still the most well-known name. The implementation of this work is available on different popular deep learning frameworks such as <a href="https://github.com/idealo/image-quality-assessment" target="_blank">Tensorflow</a>, <a href="https://github.com/titu1994/neural-image-assessment" target="_blank">Keras</a>, <a href="https://github.com/yunxiaoshi/Neural-IMage-Assessment" target="_blank">PyTorch</a>.

### Personalized approach
Besides the generic approach to the IAA problem, there are works that deal with this problem in a personalized manner. The common approach of these works is to start from a generic model mentioned in the above section, thereby using the aesthetic labeled of each individual to train a dedicated model for that person. Sometimes, it is quite expensive to collect these labeled data, even impossible. To get around this problem, some works suggest utilizing other sources of personal data such as social network usage behavior.

So, with three aspects we have just walked through, we have been introduced to a big picture of the IAA problem, about the approaches researchers used to deal with this complex problem.

<br/>

---

# <a id="discussion"></a>Discussion

At the end of the blog post, I would like to share some of my thoughts when embarking on researching this topic.

For me, the most difficult part when studying the problem of IAA is how to clearly define the criteria for aesthetic assessment; here, I only mention the criteria that are considered to be technically assessable. Sometimes, the definition of an aesthetic criterion also determines whether this criterion can be assessed objectively or not. The more clearly defined the criteria, the easier it is for humans or even machines to judge.

Until now, I still think, whether the solutions using deep learning for solving the problem of assessing image aesthetics, even though they achieve the so-called "impressive" numbers, even though they claim to be better than ones proposed in previous works, actually learned something, or simply **OVERFITTING** on the test set of a public dataset. Since deep learning models are used, there is no need to care much about how the model is learning, and what is being learned; just providing input in the right format and we will receive the output eventually.

Personally, I think it will take a long more time before researchers can understand the IAA problem as they know about image classification, object detection, etc., to get to the stage where machines surpass human capabilities, to the point where just a few percent more of a metric can determine a SOTA model. Hopefully, we will see breakthroughs in the next 5--10 years, in image aesthetics understanding and IAA problem-solving.

<center><img src="/img/academic/iaa/iaa_expectancy.png" alt="" title="" style="max-width: 100%; height: auto;"/></center>

All opinions I give here are purely based on my knowledge about IAA problem with subjective inferences; therefore, you can catch some inaccurate statements. Still waiting for comments from the community to have a deeper understanding of this interesting topic.

*See ya in the next blog post!*

<br/>

---

# <a id="references"></a>References

[1] <a id="ref-1" href="https://dictionary.cambridge.org/dictionary/english/aesthetics" target="_blank">Cambridge Dictionary</a>\
[2] <a id="ref-2" href="https://www.merriam-webster.com/dictionary/aesthetics" target="_blank">Merriam-Webster Dictionary</a>\
[3] <a id="ref-3" href="https://hal.archives-ouvertes.fr/hal-03311344/file/Subjectivity_and_Explainability_in_Image_Aesthetic_Quality_Assessment.pdf" target="_blank">Advances and Challenges in Computational Image Aesthetics</a>\
[4] <a id="ref-4" href="https://arxiv.org/pdf/2103.11616.pdf" target="_blank">A Survey on Image Aesthetic Assessment</a>\
[5] <a id="ref-5" href="https://www.cs.cmu.edu/~efros/courses/LBMV07/Papers/csurka-eccv-04.pdf" target="_blank">Visual Categorization with Bags of Keypoints</a>\
[6] <a id="ref-6" href="https://proceedings.neurips.cc/paper/1998/file/db1915052d15f7815c8b88e879465a1e-Paper.pdf" target="_blank">Exploiting Generative Models in Discriminative Classifiers</a>\
[7] <a id="ref-7" href="https://proceedings.neurips.cc/paper/2012/file/c399862d3b9d6b76c8436e924a68c45b-Paper.pdf" target="_blank">ImageNet Classification with Deep Convolutional Neural Networks</a>\
[8] <a id="ref-8" href="https://arxiv.org/pdf/1409.1556.pdf" target="_blank">Very Deep Convolutional Networks for Large-Scale Image Recognition</a>\
[9] <a id="ref-9" href="https://arxiv.org/pdf/1704.04861.pdf" target="_blank">MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications</a>\
[10] <a id="ref-10" href="https://arxiv.org/pdf/1801.04381.pdf" target="_blank">MobileNetV2: Inverted Residuals and Linear Bottlenecks</a>\
[11] <a id="ref-11" href="https://arxiv.org/pdf/1905.02244.pdf" target="_blank">Searching for MobileNetV3</a>\
[12] <a id="ref-12" href="https://arxiv.org/pdf/1512.03385.pdf" target="_blank">Deep Residual Learning for Image Recognition</a>\
[13] <a id="ref-13" href="http://yann.lecun.com/exdb/publis/pdf/chopra-05.pdf" target="_blank">Learning a Similarity Metric Discriminatively, with Application to Face Verification</a>\
[14] <a id="ref-14" href="https://arxiv.org/pdf/1412.6622.pdf" target="_blank">Deep metric learning using Triplet network</a>\
[15] <a id="ref-15" href="https://openaccess.thecvf.com/content_cvpr_2016/papers/Zhou_Learning_Deep_Features_CVPR_2016_paper.pdf" target="_blank">Learning Deep Features for Discriminative Localization</a>\
[16] <a id="ref-16" href="https://arxiv.org/pdf/1610.02391.pdf" target="_blank">Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization</a>\
[17] <a id="ref-17" href="https://arxiv.org/pdf/1606.01621.pdf" target="_blank">Photo Aesthetics Ranking Network with Attributes and Content Adaptation</a>\
[18] <a id="ref-18" href="https://arxiv.org/pdf/1908.11310.pdf" target="_blank">Aesthetic Image Captioning From Weakly-Labelled Photographs</a>\
[19] <a id="ref-19" href="https://arxiv.org/pdf/1709.05424.pdf" target="_blank">NIMA: Neural Image Assessment</a>

<hr style="border:1px solid gray">

<br/>

#### Sources of images used in this blog post
- <a href="https://xframe.io/photos/22262" target="_blank">https://xframe.io/photos/22262</a>
- <a href="https://madhansart.com/emphasis-in-art/" target="_blank">https://madhansart.com/emphasis-in-art/</a>
- <a href="https://www.flickr.com/photos/120139997@N08/14533502625/" target="_blank">https://www.flickr.com/photos/120139997@N08/14533502625/</a>
- <a href="https://www.flickr.com/photos/timw1/49061321922/" target="_blank">https://www.flickr.com/photos/timw1/49061321922/</a>
- <a href="https://www.freepik.com/free-vector/memphis-style-pattern-design_1065872.htm" target="_blank">https://www.freepik.com/free-vector/memphis-style-pattern-design_1065872.htm</a>
- <a href="https://www.pexels.com/photo/nature-bird-red-winter-46166/" target="_blank">https://www.pexels.com/photo/nature-bird-red-winter-46166/</a>
- <a href="https://www.pexels.com/photo/white-and-gray-bird-on-the-bag-of-brown-and-black-pig-swimming-on-the-beach-during-daytime-66258/" target="_blank">https://www.pexels.com/photo/white-and-gray-bird-on-the-bag-of-brown-and-black-pig-swimming-on-the-beach-during-daytime-66258/</a>
- <a href="https://www.pexels.com/photo/grey-bird-perched-on-a-tree-branch-2662434/" target="_blank">https://www.pexels.com/photo/grey-bird-perched-on-a-tree-branch-2662434/</a>
- <a href="https://www.pexels.com/photo/photo-of-yellow-and-blue-macaw-with-one-wing-open-perched-on-a-wooden-stick-2317904/" target="_blank">https://www.pexels.com/photo/photo-of-yellow-and-blue-macaw-with-one-wing-open-perched-on-a-wooden-stick-2317904/</a>
- <a href="https://www.pexels.com/photo/macro-photography-of-colorful-hummingbird-349758/" target="_blank">https://www.pexels.com/photo/macro-photography-of-colorful-hummingbird-349758/</a>
