# Session 5 

## EVA_S5_F1.ipynb
Taken from S5 - file 1 

**Basic Code + Network Structure**  
   
**Target :**  

1. 99.4% (this must be consistently shown in your last few epochs, and not a one-time achievement) **Pending**
2. Less than or equal to 15 Epochs **Done**   
3. Less than 10000 Parameters **Pending**  

**Achieved :**  ConvShape+Codestructure+Basic observations

1. Get the set-up right **Done**  
2. Set Transforms **Done**  
3. Set Data Loader **Done**  
4. Set Basic Working Code **Done**  
5. Set Basic Training  & Test Loop **Done**  
6. Experiemnt with the code **Done**  
7. Rewrite the convolutions in meaningful way **Done**  

**Results :**  

1. Epochs : **15**  
2. Parameters : **16,190**  
3. Best Train Accuracy : **96.62%**  
4. Best Test Accuracy : **98.86%**  

**Analysis :**  

1.  In the Initial Epochs, the Test acuuracy is very high compared to train accuracy - which means the model is doing quite good even at lower epochs - it might be picking up the right features early on  
2. It can be observed that the training accuracy kept on increasing through out all the epochs - which means the model is doing what it is supposed to do : learning continuously  
3. But the Test accuracy dips after some epochs - which mean that the model might be overfitting after all  
4. The Dip in the test accuracy can be observed after multiple epochs in the logs  
5. Any kind of regularization can be helpful to us in this scenario  
6. Personally, I would be happy of i do not see any kinks in the Test accuracy graph - that is no hiccups in the graph  
7. But, the number of params in the network had to be reduced first  
8. Since the Test accuracy is not trailing much behing the Train Accuracy, we might say that it is not overfitting by large  

## EVA_S5_F2.ipynb

**Basic Code + Network Structure + less channels + GAP**  

**Aim :**  
1. 99.4% (this must be consistently shown in your last few epochs, and not a one-time achievement) **Pending**
2. Less than or equal to 15 Epochs **Done**   
3. Less than 10000 Parameters **Done**  

**Achieved :**  

1. Less than 10000 Parameters **Done**  
2. Decreased the number of channels **Done**  
3. Added GAP layer **Done**  

**Results :**  

1. Epochs : **15**  
2. Parameters : **8,946**  
3. Best Train Accuracy : **98.62**  
4. Best Test Accuracy : **98.54**  

**Analysis :**  

1. Model keeps learning and can be pushed further, but it might start to overfit  
2. It might be beneficial to use a BN at this point to boost the network performance in lesser epochs
3. Model seems to not learn much in the initial 3 epochs, which must be tweaked with some dropout or BN. But this is a point of concern.  

## EVA_S5_F3.ipynb

**Basic Code + Network Structure + Less channels + GAP + BN**  

**Aim :**  
1. 99.4% (this must be consistently shown in your last few epochs, and not a one-time achievement) **Pending**
2. Less than or equal to 15 Epochs **Done**   
3. Less than 10000 Parameters **Done**  

**Achieved :**  

1. Less than 10000 Parameters   
2. Decreased the number of channels   
3. Added GAP layer  
4. Added BN in each layer  
5. BN is done before the activation  

**Results :**  

1. Epochs : **15**  
2. Parameters : **9,138**  
3. Best Train Accuracy : **99.52**  
4. Best Test Accuracy : **99.26**  

**Analysis :**  

1. In the Initial Epochs, the test accuracy picked up to a very high extent compared to previous files - which means that BN is able to help pick the right features  
2. The model can be pushed further and there seems to be signs of overfitting  
3. We can use dropout for regularization

## EVA_S5_F4.ipynb

**Basic Code + Network Structure + Less channels + GAP + BN + Dropout**  

**Aim :**  
1. 99.4% (this must be consistently shown in your last few epochs, and not a one-time achievement) **Pending**
2. Less than or equal to 15 Epochs **Done**   
3. Less than 10000 Parameters **Done**  

**Achieved :**  

1. Less than 10000 Parameters   
2. Decreased the number of channels   
3. Added GAP layer  
4. Added BN in each layer  
5. BN is done before the activation  
6. Dropout is done after the activation  

**Results :**  

1. Epochs : **15**  
2. Parameters : **8,946**  
3. Best Train Accuracy : **98.76**  
4. Best Test Accuracy : **99.16**  

**Analysis :**  

1. Dropout seems to be working as even after 15 epochs, the model can be pushed further  
2. There is still room in training to push the model  
3. At this point, we can either use Image augumentation/ LR scheduler, going with image Augumentation  
4. The reason for Image Augumentation is that we need to learn better, there might be some scenarious we are missing from the test dataset  

## EVA_S5_F5.ipynb

**Basic Code + Network Structure + Less channels + GAP + BN + Dropout**  

**Aim :**  
1. 99.4% (this must be consistently shown in your last few epochs, and not a one-time achievement) **Pending**
2. Less than or equal to 15 Epochs **Done**   
3. Less than 10000 Parameters **Done**  

**Achieved :**  

1. Less than 10000 Parameters   
2. Decreased the number of channels   
3. Added GAP layer  
4. Added BN in each layer  
5. BN is done before the activation  
6. Dropout is done after the activation  
7. RF >> image size in this scenario (final RF = 34)

**Results :**  

1. Epochs : **15**  
2. Parameters : **9,710**  
3. Best Train Accuracy : **98.37**  
4. Best Test Accuracy : **99.25**  

**Analysis :**  

1. The training can be pushed further to achieve the 99.4% in test accuracy. 
2. The model when pushed to > 15 epochs gives promising results.  
3. Accuracy improved to more than 97% in the initial epochs itself.  
