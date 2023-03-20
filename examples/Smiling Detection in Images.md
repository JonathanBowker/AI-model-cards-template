# Model Card - Smiling Detection in Images

## Model Details
- Developed by researchers at Google and the University of Toronto, 2018, v1.
- Convolutional Neural Net.
- Pretrained for face recognition then fine-tuned with cross-entropy loss for binary smiling classification.

## Intended Use
- Intended to be used for fun applications, such as creating cartoon smiles on real images; augmentative applications, such as providing details for people who are blind; or assisting applications such as automatically finding smiling photos.
- Particularly intended for younger audiences.
- Not suitable for emotion detection or determining affect; smiles were annotated based on physical appearance, and not underlying emotions.

## Factors
- Based on known problems with computer vision face technology, potential relevant factors include groups for gender, age, race, and Fitzpatrick skin type; hardware factors of camera type and lens type; and environmental factors of lighting and humidity.
- Evaluation factors are gender and age group, as annotated in the publicly available dataset CelebA [(Deep Learning Face Attributes in the Wild)](https://arxiv.org/abs/1411.7766). Further possible factors not currently available in a public smiling dataset. Gender and age determined by third-party annotators based on visual presentation, following a set of examples of male/female gender and young/old age. Further details available in [Deep Learning Face Attributes in the Wild](https://arxiv.org/abs/1411.7766).

## Metrics
- Evaluation metrics include **False Positive Rate** and **False Negative Rate** to measure disproportionate model performance errors across subgroups. **False Discovery Rate** and **False Omission Rate**, which measure the fraction of negative (not smiling) and positive (smiling) predictions that are incorrectly predicted to be positive and negative, respectively, are also reported. [Fairness Definitions Explain](https://vsahil.github.io/publication/fairness-definitions/)
- Together, these four metrics provide values for different errors that can be calculated from the confusion matrix for binary classification systems.
- These also correspond to metrics in recent definitions of “fairness” in machine learning (cf.[Fair prediction with disparate impact]( https://arxiv.org/abs/1610.07524) and [Fair prediction with disparate impact](https://arxiv.org/abs/1610.07524) and [Equality of Opportunity in Supervised Learning
](https://papers.nips.cc/paper/2016/hash/9d2682367c3935defcb1f9e247a97c0d-Abstract.html), where parity across subgroups for different metrics correspond to different fairness criteria.
- 95% confidence intervals calculated with bootstrap resampling.
- All metrics reported at the .5 decision threshold, where all error types (FPR, FNR, FDR, FOR) are within the same range (0.04 - 0.14).

## Training Data
- [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) and [Deep Learning Face Attributes in the Wild](https://arxiv.org/abs/1411.7766), training data split.

## Evaluation Data
- [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) and [Deep Learning Face Attributes in the Wild](https://arxiv.org/abs/1411.7766), test data split.
- Chosen as a basic proof-of-concept.

## Ethical Considerations
- Faces and annotations based on public figures (celebrities). No new information is inferred or annotated.

## Caveats and Recommendations
- Does not capture race or skin type, which has been reported as a source of disproportionate errors [Gender Shades: Intersectional Accuracy Disparities in Commercial Gender Classification](https://www.media.mit.edu/publications/gender-shades-intersectional-accuracy-disparities-in-commercial-gender-classification/).
- Given gender classes are binary (male/not male), which we include as male/female. Further work needed to evaluate across a spectrum of genders.
- An ideal evaluation dataset would additionally include annotations for Fitzpatrick skin type, camera details, and environment (lighting/humidity) details.

## Quantitative Analyses

![Quantitative Analysis - Smiling Detection in Images@4x](https://user-images.githubusercontent.com/1875500/226173249-54429f91-b0db-4ea6-bfb5-8b89eef6f6ca.png)
