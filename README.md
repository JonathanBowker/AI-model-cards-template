# AI & ML Model Cards
## Model Cards for Model Reporting
Model Cards serve to disclose information about a trained machine learning model. This includes how it was built, what assumptions were made during its development, what type of model behaviour different cultural, demographic, or phenotypic population groups may experience, and an evaluation of how well the model performs with respect to those groups. 


## Background
As the use of machine learning technology and AI are rapidly increasing, so too have the volume of reports of errors and failures. Despite the potentially serious repercussions of these errors, those looking to use trained machine learning models in a particular context have no way of understanding the systematic impacts of these models before deploying them or engaging their services. 

Model Cards aim to standardise ethical practice and reporting by allowing key people to compare candidate models for deployment across traditional evaluation metrics as well as the axes of ethical, inclusive, and fair considerations. This goes beyond the boundaries of current solutions that aid stakeholders in different contexts. For example, to aid policy makers and regulators on questions to ask about a model, and known benchmarks around the suitability of a model in a specific setting.

Model Cards enable model reporting with different context for those involved in different aspects of model development, deployment, and usage:

- **ML and AI practitioners** can better understand how well the model might work for its intended use cases and track its performance over time.
- **Model developers** can compare the model’s results to other models in the same space, and make decisions about training their own AI system.
- **Software developers** working on products that use the model’s predictions can inform their design and implementation decisions.
- **Policymakers** can understand how a machine learning system may fail or succeed in ways that impact individuals and groups.
- **Organisations** can make better informed decisions about adopting technology that incorporates machine learning.
- **ML-knowledgeable** individuals can be informed on different options for fine-tuning, model combination, or additional rules and constraints to help curate models for intended use cases without requiring technical expertise.
- **Impacted individuals** who may be affected by a model can better understand how it works or use information in the Model Passport to pursue remedies.

# Model Card Sections
Model Cards serve to disclose information about a trained machine learning model. This includes how it was built, what assumptions were made during its development, what type of model behaviour different cultural, demographic, or phenotypic population groups may experience, and an evaluation of how well the model performs with respect to those groups.

# ML Model Card Template
### 1. Model Details
###### Basic information about the model.
	– Developer - person or organisation developing model
	– Model date
	– Model version
	– Model type
	– Information about training algorithms, parameters, fairness constraints or other applied approaches, and features
	– References or other resource for more information
	– Citation details
	– License
	– Where to send questions or comments about the model
### 2. Intended Use
###### Use cases that were envisioned during development.
	– Primary intended uses
	– Primary intended users
	– Out-of-scope use cases
### 3. Factors
###### Factors could include demographic or phenotypic groups, environmental conditions, technical attributes, or others listed in Section 4.3.
	– Relevant factors
	– Evaluation factors
### 4. Metrics
###### Metrics should be chosen to reflect potential realworld impacts of the model.
	– Model performance measures
	– Decision thresholds
	– Variation approaches
### 5. Evaluation Data
###### Details on the dataset(s) used for the quantitative analyses in the card.
	– Datasets
	– Motivation
	– Preprocessing
### 6. Training Data
###### May not be possible to provide in practice. When possible, this section should mirror Evaluation Data. If such detail is not possible, minimal allowable information should be provided here, such as details of the distribution over various factors in the training datasets.
	– Quantitative Analyses
		– Unitary results
		– Intersectional results
	– Ethical Considerations
	– Caveats and Recommendations


# Modeal Sections
## 1. Model Details
This section of the model card should answer basic questions regarding the model version, type and other details.

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Developer**      | Which person or organisation developed the model? This can be used by all stakeholders to infer details pertaining to model development and potential conflicts of interest. |
| **Model date**     | When was the model developed? This is useful for all stakeholders to become further informed on what techniques and data sources were likely to be available during model development. |
| **Model version**      | Which version of the model is it, and how does it differ from previous versions? This is useful for all stakeholders to track whether the model is the latest version, associate known bugs to the correct model versions, and aid in model comparisons. |
| **Model type**    | What type of model is it? This includes basic model architecture details, such as whether it is a Naive Bayes classifier, a Convolutional Neural Network, etc. This is likely to be particularly relevant for software and model developers, as well as individuals knowledgeable about machine learning, to highlight what kinds of assumptions are encoded in the system. |
| **References**     | Where can resources for more information be found? Paper or other resource for more information |
| **Citations**      | How should the model be cited? License: License information can be provided. Feedback on the model: E.g., what is an email address that people may write to for further information? |

There are cases where some of this information may be sensitive. This section should not be seen as a requirement to compromise private information or reveal proprietary training techniques; rather, a place to disclose basic decisions and facts about the model that the organisation can share with the broader community in order to better inform on what the model represents.

## 2. Intended Use

This section of the model card should answer what the model should and should not be used for, and why it was created. It can also help frame the statistical analysis presented in the rest of the card, including a short description of the user(s), use-case(s), and context(s) for which the model was originally developed. This information includes but is not limited to:

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Primary intended uses** | This section details whether the model was developed with general or specific tasks in mind (e.g., plant recognition worldwide or in the Pacific Northwest). The use cases may be as broadly or narrowly defined as the developers intend. For example, if the model was built simply to label images, then this task should be indicated as the primary intended use case.|
|  **Primary intended users** | For example, was the model developed for entertainment purposes, for hobbyists, or enterprise solutions? This helps users gain insight into how robust the model may be to different kinds of inputs. |
|  **Out-of-scope uses** | Here, the model card should highlight technology that the model might easily be confused with, or related contexts that users could try to apply the model to. This section may provide an opportunity to recommend a related or similar model that was designed to better meet that particular need, where possible. This section is inspired by warning labels on food and toys, and similar disclaimers presented in electronic datasheets. Examples include “not for use on text examples shorter than 100 tokens” or “for use on black-and-white images only; please consider our research group’s full-color-image classifier for color images.” |

## 3. Factors
Model cards ideally provide a summary of model performance across a variety of relevant factors including groups, instrumentation, and environments. We briefly describe each of these factors and their relevance followed by the corresponding prompts in the model card.

### 3.1 Groups
“Groups” refers to distinct categories with similar characteristics that are present in the evaluation data instances. For human-centric machine learning models, “groups” are people who share one or multiple characteristics. Intersectional model analysis for human-centric models is inspired by the sociological concept of intersectionality, which explores how an individual’s identity and experiences are shaped not just by unitary personal characteristics – such as race, gender, sexual orientation or health – but instead by a complex combination of many factors. These characteristics, which include but are not limited to cultural, demographic and phenotypic categories, are important to consider when evaluating machine learning models. Determining which groups to include in an intersectional analysis requires examining the intended use of the model and the context under which it may be deployed. Depending on the situation, certain groups may be more vulnerable than others to unjust or prejudicial treatment.

For human-centric computer vision models, the visual presentation of age, gender, and skin type may be relevant. However, this must be balanced with the goal of preserving the privacy of individuals. As such, collaboration with policy, privacy, and legal experts is necessary in order to ascertain which groups may be responsibly inferred, and how that information should be stored and accessed. Details pertaining to groups, including who annotated the training and evaluation datasets, instructions and compensation given to annotators, and inter-annotator agreement, should be provided as part of the data documentation made available with the dataset. 

### 3.2 Instrumentation
In addition to groups, the performance of a model can vary depending on what instruments were used to capture the input to the model. For example, a face detection model may perform differently depending on the camera’s hardware and software, including lens, image stabilization, high dynamic range techniques, and background blurring for portrait mode. Performance may also vary across real or simulated traditional camera settings such as aperture, shutter speed and ISO. Similarly, video and audio input will be dependent on the choice of recording instruments and their settings. 

### 3.3 Environment
A further factor affecting model performance is the environment in which it is deployed. For example, face detection systems are often less accurate under low lighting conditions or when the air is humid. Specifications across different lighting and moisture conditions would help users understand the impacts of these environmental factors on model performance. 

### 3.4 Card Prompts
The Factors section of model cards expands on two prompts:

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Relevant factors**    |  What are foreseeable salient factors for which model performance may vary, and how were these determined? |
| **Evaluation factors**    |  Which factors are being reported, and why were these chosen? If the relevant factors and evaluation factors are different, why? For example, while Fitzpatrick skin type is a relevant factor for face detection, an evaluation dataset annotated by skin type might not be available until reporting model performance across groups becomes standard practice. |

## 4. Metrics
The appropriate metrics to feature in a model card depend on the type of model that is being tested. For example, classification systems in which the primary output is a class label differ significantly from systems whose primary output is a score. In all cases, the reported metrics should be determined based on the model’s structure and intended use. Details for this section include:

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Model performance measures**    | What measures of model performance are being reported, and why were they selected over other measures of model performance?  |
| **Decision thresholds**  | If decision thresholds are used, what are they, and why were those decision thresholds chosen? When the model card is presented in a digital format, a threshold slider should ideally be available to view performance parameters across various decision thresholds.  |
| **Approaches to uncertainty and variability**  | How are the measurements and estimations of these metrics calculated? For example, this may include standard deviation, variance, confidence intervals, or KL divergence. Details of how these values are approximated should also be included (e.g., average of 5 runs, 10-fold cross-validation).  |

### 4.1 Classification systems. 
For classification systems, the error types that can be derived from a confusion matrix are false positive rate, false negative rate, false discovery rate, and false omission rate. We note that the relative importance of each of these metrics is system, product and context dependent. 

For example, in a surveillance scenario, surveillors may value a low false negative rate (or the rate at which the surveillance system fails to detect a person or an object when it should have). On the other hand, those being surveilled may value a low false positive rate (or the rate at which the surveillance system detects a person or an object when it should not have). We recommend listing all values and providing context about which were prioritized during development and why. 

Equality between some of the different confusion matrix metrics is equivalent to some definitions of fairness. For example, equal false negative rates across groups is equivalent to fulfilling Equality of Opportunity, and equal false negative and false positive rates across groups is equivalent to fulfilling Equality of Odds

### 4.2 Score-based analyses
For score-based systems such as pricing models and risk assessment algorithms, describing differences in the distribution of measured metrics across groups may be helpful. For example, reporting measures of central tendency such as the mode, median and mean, as well as measures of dispersion or variation such as the range, quartiles, absolute deviation, variance and standard deviation could facilitate the statistical commentary necessary to make more informed decisions about model development. A model card could even extend beyond these summary statistics to reveal other measures of differences between distributions such as cross entropy, perplexity, KL divergence and pinned area under the curve. 

There are a number of applications that do not appear to be score-based at first glance, but can be considered as such for the purposes of intersectional analysis. For instance, a model card for a translation system could compare [BLEU scores across demographic groups](https://research.google/pubs/pub46743/), and a model card for a speech recognition system could compare word-error rates. Although the primary outputs of these systems are not scores, looking at the score differences between populations may yield meaningful insights since comparing raw inputs quickly grows too complex.

### 4.3 Confidence. 
Performance metrics that are disaggregated by various combinations of instrumentation, environments and groups makes it especially important to understand the confidence intervals for the reported metrics. Confidence intervals for metrics derived from confusion matrices can be calculated by treating the matrices as [probabilistic models of system performance](https://link.springer.com/chapter/10.1007/978-3-540-31865-1_25).

## 5. Evaluation Data
All referenced datasets would ideally point to any set of documents that provide visibility into the source and composition of the dataset. Evaluation datasets should include datasets that are publicly available for third-party use. These could be existing datasets or new ones provided alongside the model card analyses to enable further benchmarking. Potential details include:

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Datasets**     | What datasets were used to evaluate the model?  |
| **Motivation**  | Why were these datasets chosen?   |
| **Preprocessing**  | How was the data preprocessed for evaluation (e.g., tokenization of sentences, cropping of images, any filtering such as dropping images without faces)?  |

To ensure that model cards are statistically accurate and verifiable, the evaluation datasets should not only be representative of the model’s typical use cases but also anticipated test scenarios and challenging cases. For instance, if a model is intended for use in a workplace that is phenotypically and demographically homogeneous, and trained on a dataset that is representative of the expected use case, it may be valuable to evaluate that model on two evaluation sets: one that matches the workplace’s population, and another set that contains individuals that might be more challenging for the model (such as children, the elderly, and people from outside the typical workplace population). This methodology can highlight pathological issues that may not be evident in more routine testing. 

It is often difficult to find datasets that represent populations outside of the initial domain used in training. In some of these situations, synthetically generated datasets may provide representation for use cases that would otherwise go unevaluated.

## 6. Training Data
Ideally, the model card would contain as much information about the training data as the evaluation data. However, there might be cases where it is not feasible to provide this level of detailed information about the training data. For example, the data may be proprietary, or require a non-disclosure agreement. In these cases, we advocate for basic details about the distributions over groups in the data, as well as any other details that could inform stakeholders on the kinds of biases the model may have encoded.

## 7. Quantitative Analyses
Quantitative analyses should be disaggregated or broken down by the chosen factors. Quantitative analyses should provide the results of evaluating the model according to the chosen metrics, providing confidence interval values when possible. Parity on the different metrics across disaggregated population subgroups corresponds to how fairness is often defined. Quantitative analyses should demonstrate the metric variation (e.g., with error bars), as discussed in Section 4.4 and visualized in Figure 2. The disaggregated evaluation includes: 

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Unitary results**      | How did the model perform with respect to each factor?  |
| **Intersectional results**  | How did the model perform with respect to the intersection of evaluated factors?   |


## 8. Ethical Considerations
This section is intended to demonstrate the ethical considerations that went into model development, surfacing ethical challenges and solutions to stakeholders. Ethical analysis does not always lead to precise solutions, but the process of ethical contemplation is worthwhile to inform on responsible practices and next steps in future work. 

While there are many frameworks for ethical decision-making in technology that can be adapted, the following are specific questions for exploring in this section: 

| **Subject**        | **Question**           |
| :------------- |:--------------------------------------|
| **Data**      | Does the model use any sensitive data (e.g., protected classes)? |
| **Human life**  | Is the model intended to inform decisions about matters central to human life or flourishing – e.g., health or safety? Or could it be used in such a way?   |
| **Mitigations** | What risk mitigation strategies were used during model development?  | 
| **Risks and harms** | What risks may be present in model usage? Try to identify the potential recipients, likelihood, and magnitude of harms. If these cannot be determined, note that they were considered but remain unknown.  | 
| **Use cases** | Are there any known model use cases that are especially fraught? This may connect directly to the intended use section of the model card.  | 


## 9. Caveats and Recommendations
This section should list additional concerns that were not covered in the previous sections. For example, did the results suggest any requiremnt for further testing? Were there any relevant groups that were not represented in the evaluation dataset? Are there additional recommendations for model use? What are the ideal characteristics of an evaluation dataset for this model?

# Model Card Usage
Model Cards provide information about the context of a machine learning model, as well as model performance results disaggregated by different unitary and intersectional population groups. Model Cards are designed to accompany a specific model after careful review has determined that the foreseeable benefits outweigh the foreseeable risks in the model’s use or release.

The framework is intended to be general enough to be applicable across different institutions, contexts, and stakeholders. It also is suitable for recently proposed requirements for analysis of algorithmic decision systems in critical social institutions, for example, for models used in determining government benefits, employment evaluations, criminal risk assessment, and criminal DNA analysis. 

Model cards are just one approach to increasing transparency between developers, users, and stakeholders of machine learning models and systems. They are designed to be flexible in both scope and specificity in order to accommodate the wide variety of machine learning model types and potential use cases. Therefore the usefulness and accuracy of a model card relies on the integrity of the creator(s) of the card itself. It seems unlikely, at least in the near term, that model cards could be standardised or formalised to a degree needed to prevent misleading representations of model results (whether intended or unintended). It is therefore important to consider model cards as a transparency tool among many, which could include, for example, algorithmic auditing by third-parties (both quantitative and qualitative), “adversarial testing” by technical and non-technical analysts, and more inclusive user feedback mechanisms. 
