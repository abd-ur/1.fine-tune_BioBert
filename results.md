## Instructed hyperparameters
| Parameter           | Value             |
| ------------------- | ----------------- |
| Epochs              | 3                 |
| Batch Size          | 16                |
| Learning Rate       | 2e-5              |
| LoRA Rank           | 8                 |
| Target Modules      | query, value      |
| Evaluation Strategy | End of each epoch |


## Results
| Metric                     | Value  |
| -------------------------- | ------ |
| **Epoch**                  | 3.0    |
| **Evaluation Loss**        | 3.2504 |
| **Evaluation Accuracy**    | 0.0909 |
| **Evaluation Runtime (s)** | 0.1542 |
| **Samples per Second**     | 71.217 |
| **Steps per Second**       | 6.484  |

Even for just 3 epochs, LoRA test gave similar results but with faster compute time as below:
| Metric                     | Value  |
| -------------------------- | ------ |
| **Epoch**                  | 3.0    |
| **Evaluation Loss**        | 3.2504 |
| **Evaluation Accuracy**    | 0.0909 |
| **Evaluation Runtime (s)** | 0.1211 |
| **Eval Samples/sec**       | 60.85  |
| **Eval Steps/sec**         | 5.466  |


## Discussion:
Low accuracy and high loss due to constrained hyperparameter. Model as complex as BioBERT requires more refined hyperparameters. For test run in last cell, model outputs 3 top predictions for a query alont with cited recommendation. All three of them have around 0.05 score/probability showing need for more refined training in contrast to low volume of data and minimal hyperparameter provision.
| Query                            | Output  |
| -------------------------------- | ------- |
| TP53 p.R248W in breast cancer?   | Truncating variant; Radiation not advised. [OncoKB]: 0.0615 <br /> Truncating variant; Radiation not advised. [COSMIC]: 0.0537 <br /> Resistance mutation; Switch to alternative TKI. [ClinVar]: 0.0527 |
