# CIBMTR---Equity-in-post-HCT-Survival-Predictions

# Overview

In this competition, you’ll develop models to improve the prediction of transplant survival rates for patients undergoing allogeneic Hematopoietic Cell Transplantation (HCT) — an important step in ensuring that every patient has a fair chance at a successful outcome, regardless of their background.

# Description
Improving survival predictions for allogeneic HCT patients is a vital healthcare challenge. Current predictive models often fall short in addressing disparities related to socioeconomic status, race, and geography. Addressing these gaps is crucial for enhancing patient care, optimizing resource utilization, and rebuilding trust in the healthcare system.

This competition aims to encourage participants to advance predictive modeling by ensuring that survival predictions are both precise and fair for patients across diverse groups. By using synthetic data—which mirrors real-world situations while protecting patient privacy—participants can build and improve models that more effectively consider diverse backgrounds and conditions.

You’re challenged to develop advanced predictive models for allogeneic HCT that enhance both accuracy and fairness in survival predictions. The goal is to address disparities by bridging diverse data sources, refining algorithms, and reducing biases to ensure equitable outcomes for patients across diverse race groups. Your work will help create a more just and effective healthcare environment, ensuring every patient receives the care they deserve.

# Evaluation
# Evaluation Criteria
The evaluation of prediction accuracy in the competition will involve a specialized metric known as the Stratified Concordance Index (C-index), adapted to consider different racial groups independently. This method allows us to gauge the predictive performance of models in a way that emphasizes equitability across diverse patient populations, particularly focusing on racial disparities in transplant outcomes.

# Concordance index
It represents the global assessment of the model discrimination power: this is the model’s ability to correctly provide a reliable ranking of the survival times based on the individual risk scores. It can be computed with the following formula:

![image](https://github.com/user-attachments/assets/4d2a3890-6363-4ab2-b821-4503a12e1b9f)

The concordance index is a value between 0 and 1 where:

0.5 is the expected result from random predictions,

1.0 is a perfect concordance and,

0.0 is perfect anti-concordance (multiply predictions with -1 to get 1.0)

# Stratified Concordance Index

For this competition, we adjust the standard C-index to account for racial stratification, thus ensuring that each racial group's outcomes are weighed equally in the model evaluation. The stratified c-index is calculated as the mean minus the standard deviation of the c-index scores calculated within the recipient race categories, i.e., the score will be better if the mean c-index over the different race categories is large and the standard deviation of the c-indices over the race categories is small. This value will range from 0 to 1, 1 is the theoretical perfect score, but this value will practically be lower due to censored outcomes.

The submitted risk scores will be evaluated using the score function. This evaluation process involves comparing the submitted risk scores against actual observed values (i.e., survival times and event occurrences) from a test dataset. The function specifically calculates the stratified concordance index across different racial groups, ensuring that the predictions are not only accurate overall but also equitable across diverse patient demographics.

# Background Information
# What is an allogeneic HCT?
The human immune system comprises cells that develop from hematopoietic stem cells, a special type of cells that reside in the bone marrow. These stem cells are responsible for generating all blood cells, including red blood cells, platelet-producing cells, and immune system cells such as T cells, B cells, neutrophils, and natural killer (NK) cells. Allogeneic hematopoietic cell transplantation (HCT) can be used to replace an individual's faulty hematopoietic stem cells with stem cells that can produce normal immune system cells. In other words, a successful HCT can help fix a person's immune system by introducing healthy stem cells into their body. When hematopoietic stem cells are transferred from one person to another, the recipient is referred to as the HCT recipient. The term "allogeneic" indicates that the stem cells being used come from someone else, the hematopoietic stem cell donor. If the HCT is successful, the donor's hematopoietic stem cells will replace the recipient's cells, producing blood and immune system cells that work correctly.

The source of hematopoietic stem cells can be bone marrow, peripheral blood, or umbilical cord blood. Depending on the source of the stem cells, HCT procedures may be called bone marrow transplants (BMT), peripheral blood stem cell transplants, or cord blood transplants.

More information on how blood stem cell transplants work.

The competition hosts CIBMTR and NMDP have saved over 130,000 lives through cell therapy.
