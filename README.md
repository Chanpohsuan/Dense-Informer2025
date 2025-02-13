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
<table>
  <tr>
    <td>Parameter name</td>
    <td>Description of parameter</td>
  </tr>
  <tr>
    <td>model</td>
    <td>The model of experiment. This can be set to Dense-informer</td>
  </tr>
  <tr>
    <td>data</td>
    <td>The dataset name</td>
  </tr>
  <tr>
    <td>features</td>
    <td>The forecasting task (defaults to M). This can be set to M,S,MS (M : multivariate predict multivariate, S : univariate predict univariate, MS : multivariate predict univariate)</td>
  </tr>
  <tr>
    <td>target</td>
    <td>Target feature in S or MS task (defaults to OT)</td>
  </tr>
   <tr>
    <td>freq</td>
    <td>Freq for time features encoding (defaults to h). This can be set to s,t,h,d,b,w,m (s:secondly, t:minutely, h:hourly, d:daily, b:business days, w:weekly, m:monthly).You can also use more detailed freq like 15min or 3h</td>
  </tr>
  <tr>
    <td>seq_len</td>
    <td>Input sequence length of Informer encoder (defaults to 96)</td>
  </tr>
  <tr>
    <td>label_len</td>
    <td>Start token length of Informer decoder (defaults to 48)</td>
  </tr>
  <tr>
    <td>pred_len</td>
    <td>Prediction sequence length (defaults to 24)</td>
  </tr>
  <tr>
    <td>d_model	</td>
    <td>Dimension of model (defaults to 512)</td>
  </tr>
  <tr>
    <td>n_heads</td>
    <td>Num of heads (defaults to 8)</td>
  </tr>
  <tr>
    <td>e_layers</td>
    <td>Num of encoder layers (defaults to 3)</td>
  </tr>
  <tr>
    <td>d_layers</td>
    <td>Num of decoder layers (defaults to 2)</td>
  </tr>
  <tr>
    <td>d_ff</td>
    <td>Dimension of fcn (defaults to 2048)</td>
  </tr>
  <tr>
    <td>factor</td>
    <td>Probsparse attn factor (defaults to 5)</td>
  </tr>
  <tr>
    <td>padding</td>
    <td>Padding type(defaults to 0).</td>
  </tr>
  <tr>
    <td>attn</td>
    <td>Attention used in encoder (defaults to prob). This can be set to prob (informer), full (transformer)</td>
  </tr>
  <tr>
    <td>embed</td>
    <td>Time features encoding (defaults to timeF). This can be set to timeF, fixed, learned</td>
  </tr>
  <tr>
    <td>activation</td>
    <td>Activation function (defaults to gelu)</td>
  </tr>
  <tr>
    <td>batch_size</td>
    <td>The batch size of training input data (defaults to 32)</td>
  </tr>
  <tr>
    <td>patience</td>
    <td>Early stopping patience (defaults to 3)</td>
  </tr>
  <tr>
    <td>learning_rate</td>
    <td>Optimizer learning rate (defaults to 0.0001)</td>
  </tr>
  <tr>
    <td>des</td>
    <td>Experiment description (defaults to test)</td>
  </tr>
  <tr>
    <td>loss</td>
    <td>Loss function (defaults to MSE_Loss*0.2+Charbonnier_Loss*0.8)</td>
  </tr>
  <tr>
    <td>lradj</td>
    <td>Ways to adjust the learning rate (defaults to type1)</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
</table>

##Results
we have updated the experiment results of all methods due to the change in data scaling
![image](https://github.com/Chanpohsuan/Dense-Informer2025/blob/main/2.png](https://github.com/Chanpohsuan/Dense-Informer2025/blob/main/3.png)

##Contact
If you have any questions, feel free to contact Chan through Email (www904083@gmail.com) or Github issues. Pull requests are highly welcomed!

