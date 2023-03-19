# AI and ML Model Cards
AI and ML Model Cards serve to disclose information about a trained machine learning model. This includes how it was built, what assumptions were made during its development, what type of model behaviour different cultural, demographic, or phenotypic population groups may experience, and an evaluation of how well the model performs with respect to those groups. 


# Background
As the use of machine learning technology has rapidly increased, so too have reports of errors and failures. Despite the potentially serious repercussions of these errors, those looking to use trained machine learning models in a particular context have no way of understanding the systematic impacts of these models before deploying them.

Model Cards aim to standardise ethical practice and reporting - allowing stakeholders to compare candidate models for deployment across not only traditional evaluation metrics but also along the axes of ethical, inclusive, and fair considerations. This goes further than current solutions to aid stakeholders in different contexts. For example, to aid policy makers and regulators on questions to ask of a model, and known benchmarks around the suitability of a model in a given setting.

Model reporting will hold different meaning to those involved in different aspects of model development, deployment, and use. Below, we outline a few use cases for different stakeholders:

- ML and AI practitioners can better understand how well the model might work for the intended use cases and track its performance over time.
- Model developers can compare the model’s results to other models in the same space, and make decisions about training their own system.
- Software developers working on products that use the model’s predictions can inform their design and implementation decisions.
- Policymakers can understand how a machine learning system may fail or succeed in ways that impact people.
- Organisations can inform decisions about adopting technology that incorporates machine learning.
- ML-knowledgeable individuals can be informed on different options for fine-tuning, model combination, or additional rules and constraints to help curate models for intended use cases without requiring technical expertise.
- Impacted individuals who may experience effects from a model can better understand how it works or use information in the card to pursue remedies.

# Model Card Sections
Model cards serve to disclose information ab

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
When possible, this section should mirror Evaluation Data. If such detail is not possible, minimal allowable information should be provided here, such as details of the distribution over various factors in the training datasets.
– Quantitative Analyses
	– Unitary results
	– Intersectional results
– Ethical Considerations
– Caveats and Recommendations
