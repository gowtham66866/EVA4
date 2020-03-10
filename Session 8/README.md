
# CIFAR 10 : Classification using RESNET18

## Index  
1. [Objective](#objective)  
2. [Model Summary](#model-summary)
3. [Result Summary](#result-summary)
4. [Result Visualizations](#result-visualizations) (misclassification/accuracy/loss)

## Objective   
1. Code uses GPU - **Done**  
2. Use the architecture to RESNET18 - **Done**  
3. Achieve 85% accuracy, with no limit on no of parameters - **Done**   
4. All the code is split and individual modules are called upon for execution - **Done**    

## Model Summary  

![Model Summary](./images/Model_Summary.png)

## Result Summary

The following image gives an idea of which model seems to achieve the best Validation Accuracy.


| Model | Train Accuracy | Test Accuracy |
| --- | --- | --- |
| ResNet18 - Normal | 98.98 | 88.42 |
| ResNet18 - L1 | 82.61| 81.08 |
| ResNet18 - L2 | 98.85 | 88.70 |
| ResNet18 - ElastiNet | 82.60 | 81.31 |

## Result Visualizations

### Validation Accuracy   
![Validation Accuracy](./images/Validation_Accuracy.png)

### Validation Loss  
![Validation Loss](./images/Validation_Loss.png)

### 25 misclassified images for L2 : Best Model  
![L2 misclassified](./images/Val_L2_Misclassification.png)

