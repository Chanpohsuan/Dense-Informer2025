# Stock Price Prediction Based on The Informer Network with Dense Connections!

![image](https://github.com/Chanpohsuan/Dense-Informer2025/blob/main/1.jpg)

## Environment requirement
Google_Colab

## Preparation
Download dataset
The  dataset used in the paper can be downloaded in the repo [Dataset](https://github.com/Chanpohsuan/Dense-Informer2025/tree/main/data). The required data files should be name 'output'. A demo slice of the  data is illustrated in the following figure. Note that the input of each dataset is zero-mean normalized in this implementation.
![image](https://github.com/Chanpohsuan/Dense-Informer2025/blob/main/2.png)

## Training
run Dense-informer.ipynb
##Usage
The detailed descriptions about the arguments are as following:
Parameter name	Description of parameter
model	The model of experiment. This can be set to informer, informerstack, informerlight(TBD)
data	The dataset name
root_path	The root path of the data file (defaults to ./data/ETT/)
data_path	The data file name (defaults to ETTh1.csv)
features	The forecasting task (defaults to M). This can be set to M,S,MS (M : multivariate predict multivariate, S : univariate predict univariate, MS : multivariate predict univariate)
target	Target feature in S or MS task (defaults to OT)
freq	Freq for time features encoding (defaults to h). This can be set to s,t,h,d,b,w,m (s:secondly, t:minutely, h:hourly, d:daily, b:business days, w:weekly, m:monthly).You can also use more detailed freq like 15min or 3h
checkpoints	Location of model checkpoints (defaults to ./checkpoints/)
seq_len	Input sequence length of Informer encoder (defaults to 96)
label_len	Start token length of Informer decoder (defaults to 48)
pred_len	Prediction sequence length (defaults to 24)
enc_in	Encoder input size (defaults to 7)
dec_in	Decoder input size (defaults to 7)
c_out	Output size (defaults to 7)
d_model	Dimension of model (defaults to 512)
n_heads	Num of heads (defaults to 8)
e_layers	Num of encoder layers (defaults to 2)
d_layers	Num of decoder layers (defaults to 1)
s_layers	Num of stack encoder layers (defaults to 3,2,1)
d_ff	Dimension of fcn (defaults to 2048)
factor	Probsparse attn factor (defaults to 5)
padding	Padding type(defaults to 0).
distil	Whether to use distilling in encoder, using this argument means not using distilling (defaults to True)
dropout	The probability of dropout (defaults to 0.05)
attn	Attention used in encoder (defaults to prob). This can be set to prob (informer), full (transformer)
embed	Time features encoding (defaults to timeF). This can be set to timeF, fixed, learned
activation	Activation function (defaults to gelu)
output_attention	Whether to output attention in encoder, using this argument means outputing attention (defaults to False)
do_predict	Whether to predict unseen future data, using this argument means making predictions (defaults to False)
mix	Whether to use mix attention in generative decoder, using this argument means not using mix attention (defaults to True)
cols	Certain cols from the data files as the input features
num_workers	The num_works of Data loader (defaults to 0)
itr	Experiments times (defaults to 2)
train_epochs	Train epochs (defaults to 6)
batch_size	The batch size of training input data (defaults to 32)
patience	Early stopping patience (defaults to 3)
learning_rate	Optimizer learning rate (defaults to 0.0001)
des	Experiment description (defaults to test)
loss	Loss function (defaults to mse)
lradj	Ways to adjust the learning rate (defaults to type1)
use_amp	Whether to use automatic mixed precision training, using this argument means using amp (defaults to False)
inverse	Whether to inverse output data, using this argument means inversing output data (defaults to False)
use_gpu	Whether to use gpu (defaults to True)
gpu	The gpu no, used for training and inference (defaults to 0)
use_multi_gpu	Whether to use multiple gpus, using this argument means using mulitple gpus (defaults to False)
devices	Device ids of multile gpus (defaults to 0,1,2,3)
