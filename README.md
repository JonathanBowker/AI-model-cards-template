# AI and ML Model Cards
## Model Cards for Model Reporting
AI and ML Model Cards serve to disclose information about a trained machine learning model. This includes how it was built, what assumptions were made during its development, what type of model behaviour different cultural, demographic, or phenotypic population groups may experience, and an evaluation of how well the model performs with respect to those groups. 


# Background
As the use of machine learning technology has rapidly increased, so too have reports of errors and failures. Despite the potentially serious repercussions of these errors, those looking to use trained machine learning models in a particular context have no way of understanding the systematic impacts of these models before deploying them.

Model Cards standardise ethical practice and reporting by allowing stakeholders to compare candidate models for deployment across traditional evaluation metrics, and along the axes of ethical, inclusive, and fair considerations. This goes further than current solutions to aid stakeholders in different contexts. For example, to aid policy makers and regulators on questions to ask of a model, and known benchmarks around the suitability of a model in a given setting.

This enables model reporting with different meanings to those involved (see below) in different aspects of model development, deployment, and use:

- ML and AI practitioners can better understand how well the model might work for the intended use cases and track its performance over time.
- Model developers can compare the model’s results to other models in the same space, and make decisions about training their own system.
- Software developers working on products that use the model’s predictions can inform their design and implementation decisions.
- Policymakers can understand how a machine learning system may fail or succeed in ways that impact people.
- Organisations can inform decisions about adopting technology that incorporates machine learning.
- ML-knowledgeable individuals can be informed on different options for fine-tuning, model combination, or additional rules and constraints to help curate models for intended use cases without requiring technical expertise.
- Impacted individuals who may experience effects from a model can better understand how it works or use information in the card to pursue remedies.

# Model Card Sections
Model cards serve to disclose information about the 

# ML Model Card
### Model Details. Basic information about the model.
	– Person or organization developing model
	– Model date
	– Model version
	– Model type
	– Information about training algorithms, parameters, fairness constraints or other applied approaches, and features
	– Paper or other resource for more information
	– Citation details
	– License
	– Where to send questions or comments about the model
### Intended Use. Use cases that were envisioned during development.
	– Primary intended uses
	– Primary intended users
	– Out-of-scope use cases
### Factors. Factors could include demographic or phenotypic groups, environmental conditions, technical attributes, or others listed in Section 4.3.
	– Relevant factors
	– Evaluation factors
### Metrics. Metrics should be chosen to reflect potential realworld impacts of the model.
	– Model performance measures
	– Decision thresholds
	– Variation approaches
### Evaluation Data. Details on the dataset(s) used for the quantitative analyses in the card.
	– Datasets
	– Motivation
	– Preprocessing
### Training Data. May not be possible to provide in practice.
##### When possible, this section should mirror Evaluation Data. If such detail is not possible, minimal allowable information should be provided here, such as details of the distribution over various factors in the training datasets.
	– Quantitative Analyses
		– Unitary results
		– Intersectional results
	– Ethical Considerations
	– Caveats and Recommendations


# Model Details

### Person or organization developing model 
What person or organization developed the model? This can be used by all stakeholders to infer details pertaining to model development and potential conflicts of interest.

### Model date
When was the model developed? This is useful for all stakeholders to become further informed on what techniques and data sources were likely to be available during model development.

### Model version
Which version of the model is it, and how does it differ from previous versions? This is useful for all stakeholders to track whether the model is the latest version, associate known bugs to the correct model versions, and aid in model comparisons.

### Model type
What type of model is it? This includes basic model architecture details, such as whether it is a Naive Bayes classifier, a Convolutional Neural Network, etc. This is likely to be particularly relevant for software and model developers, as well as individuals knowledgeable about machine learning, to highlight what kinds of assumptions are encoded in the system.

### Paper or other resource for more information
Where can resources for more information be found?

### Citation details
How should the model be cited? License: License information can be provided. Feedback on the model: E.g., what is an email address that people may write to for further information?

There are cases where some of this information may be sensitive. This section should not be seen as a requirement to compromise private information or reveal proprietary training techniques; rather, a place to disclose basic decisions and facts about the model that the organisation can share with the broader community in order to better inform on what the model represents.

# Intended Use

The model should and should not be used for, and why it was created. It can also help frame the statistical analysis presented in the rest of the card, including a short description of the user(s), use-case(s), and context(s) for which the model was originally developed. Possible information includes:

### Primary intended uses
This section details whether the model was developed with general or specific tasks in mind (e.g., plant recognition worldwide or in the Pacific Northwest). The use cases may be as broadly or narrowly defined as the developers intend. For example, if the model was built simply to label images, then this task should be indicated as the primary intended use case. 

### Primary intended users
For example, was the model developed for entertainment purposes, for hobbyists, or enterprise solutions? This helps users gain insight into how robust the model may be to different kinds of inputs.

### Out-of-scope uses
Here, the model card should highlight technology that the model might easily be confused with, or related contexts that users could try to apply the model to. This section may provide an opportunity to recommend a related or similar model that was designed to better meet that particular need, where possible. This section is inspired by warning labels on food and toys, and similar disclaimers presented in electronic datasheets. Examples include “not for use on text examples shorter than 100 tokens” or “for use on black-and-white images only; please consider our research group’s full-color-image classifier for color images.”
