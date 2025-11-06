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
Low accuracy and high loss due to constrained hyperparameter. Model as complex as BioBERT requires more refined hyperparameters. For test run in last cell, model predicts wrong output due to low volume of data, and minimal hyperparameter provision.
