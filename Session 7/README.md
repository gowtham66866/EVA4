# CIFAR 10 : Classification

## Index  
1. [Target](#target)  
2. [Receptive Field Calculations](#receptive-field-calculations)
3. [Result Summary](#result-summary)


## Target   
1. Code uses GPU - **Done**  
2. Use the architecture to C1,C2,C3,C4,O (basically 3 MPs) - **Done**  
3. Total RF must be more than 44 - **Done(RF = 96)**  
4. One of the layers must use Depthwise Separable Convolution - **Done**  
5. One of the layers must use Dilated Convolution  - **Done**  
6. Use GAP (compulsory):- add FC after GAP to target #of classes (optional) - **Done**  
7. Achieve 80% accuracy, as many epochs as you want. Total Params to be less than 1M - **Done**   

## Receptive Field Calculations 

-------Net summary------   
* input image:     
	+ n features: 32   
	+ jump: 1    
	+ receptive size: 1    
	+ start: 0.5    
* conv1:   
	+ n features: 30    
	+ jump: 1    
	+ receptive size: 3    
	+ start: 1.5    
* conv2:   
	+ n features: 36    
	+ jump: 1    
	+ receptive size: 5    
	+ start: -1.5    
* conv3:   
	+ n features: 44    
	+ jump: 1    
	+ receptive size: 5    
	+ start: -5.5    
* MP1:   
	+ n features: 22    
	+ jump: 2    
	+ receptive size: 6    
	+ start: -5.0    
* conv4:   
	+ n features: 22    
	+ jump: 2    
	+ receptive size: 6    
	+ start: -5.0    
* conv5:
	+ n features: 22    
	+ jump: 2    
	+ receptive size: 14    
	+ start: -5.0    
* conv6:   
	+ n features: 22    
	+ jump: 2    
	+ receptive size: 22    
	+ start: -5.0    
* conv7:   
	+ n features: 22    
	+ jump: 2    
	+ receptive size: 30    
	+ start: -5.0    
* MP2:   
	+ n features: 11    
	+ jump: 4    
	+ receptive size: 32    
	+ start: -4.0    
* conv8:   
	+ n features: 11    
	+ jump: 4    
	+ receptive size: 32    
	+ start: -4.0    
* conv9:   
	+ n features: 11    
	+ jump: 4    
	+ receptive size: 48    
	+ start: -4.0    
* conv10:   
	+ n features: 11    
	+ jump: 4    
	+ receptive size: 64    
	+ start: -4.0    
* GAP:   
	+ n features: 1    
	+ jump: 36    
	+ receptive size: 96    
	+ start: 16.0    
* conv11:   
	+ n features: 1    
	+ jump: 36    
	+ receptive size: 96    
	+ start: 16.0    

------------------------    

## Result Summary

# Validation Accuracy   
![Validation Accuracy](./Test_Accuracy.png)

# Validation Loss  
![Validation Loss](./Test_Loss.png)

# 25 misclassified images for L1  
![L1 misclassified](./L1_Test.png)

# 25 misclassified images for L2  
![L1 misclassified](./L2_Test.png)

