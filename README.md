# EVA_S5

Goal is to build a Deep learning model on MNIST data which achieves Test Accuracy of minimum 99.4% in less than 16 epochs and less than 10K parameters used in Five step by step procedure.

Following is the strategy followed for each of five steps and their results:

#Step1: S5_F1_Basic Setup

Target:
  Get the set-up right
  Set Transforms
  Set Data Loader
  Set Basic Working Code
  Set Basic Training  & Test Loop
  
Results:
  Parameters: 12,096
  Best Training Accuracy: 99.11%
  Best Test Accuracy: 98.71%
  
Analysis:
  1. There is little overfitting.
  2. Model can be pushed to achieve higher Accuracy, if overfitting exists then Regularise.

Step2:S5_F2_BatchNormalise

Target:
  Increase efficiency of the model by adding Batch Normalisation 

Results:
  Parameters: 12,276
  Best Train Accuracy: 99.81%
  Best Test Accuracy: 98.09%

Analysis:
  1.Achieved good accuracy but overfitting persists
  2.Regularisation of model may help

Step3: S5_F3_Regularization

Target:
  Reduce Overfit by adding Regularization i.e Dropout

Results:
  Parameters: 12,276
  Best Train Accuracy: 99.19% (15th Epoch)
  Best Train Accuracy: 99.19%

Analysis:
  Regularization worked.
  Very good model at 15th epoch but train and test accuracies oscillating around 99.25%-99.31% and suddenly landed at 99.19 in just 15th   epoch

Step4: S5_F4_GAP_Layer.ipynb

Target:
  Model efficiency can be improved in more number of epochs likely. But as we contrained on 15 epochs and 10K parameters, add gap layer   to replace big kernel at end

Results:
  Parameters: 11,012
  Best Train Accuracy: 99.03% 
  Best Train Accuracy: 99.42%

Analysis:
  1. Model is underfit and able to achieve accuracy of 99.4%
  2. Lighten the model by reducing the channels to bring the parameters to less than 10K

Step5: S5_F5_Lighten_the_model

Target:
  Lighten the Model

Results:
  Parameters: 9,704
  Best Train Accuracy: 98.97% 
  Best Train Accuracy: 99.39%

Analysis:
  1. Model is still underfit but accuracy is getting disrupted with reduction of channels
