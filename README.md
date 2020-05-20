# Neural Machine Translation(ENG - ITA)

The objective of this project is to convert an **English** sentence to it's **Italian** counterpart using a Neural Machine Translation system. I will implement this task by building a simple encoder-decoder model.

## Resources Used

* **Python version :** 3.7
* **Tensorflow version :** 2.2
* **Packages Used :** numpy,pandas,seaborn,sklearn,tensorflow,nltk

## Exploratory Data Analysis

I did EDA to check the distribution of the data based on word count. To even things out and also because of memory reasons , i removed sentences having word count greater than 13.
![Machine translation pic](https://user-images.githubusercontent.com/42802226/82417096-ae685100-9a98-11ea-870f-d20bc69f8576.png)

## Model Building

This project was built using a simple **Encoder-Decoder** model.
Encoder reads the input sequence and summarizes the information in something called as the **internal state vectors** (in case of LSTM these are called as the hidden state and cell state vectors). We discard the outputs of the encoder and only preserve the internal states.
Decoder is an LSTM whose initial states are initialized to the **final states of the Encoder LSTM**. Using these initial states, decoder starts generating the output sequence.  

To simplify things, here is a small image.
![NMT](https://user-images.githubusercontent.com/42802226/82417678-84fbf500-9a99-11ea-83da-2476470992d9.png)  

## Model performance

I ran the model for only 40 epochs due to the fact that Google Colab only provides 12GB of RAM. More than 40 epochs would result in Google Colab crashing.  
**Even though the model ran for only 40 epochs , It produced pretty good results!.**  
Here are a few examples.  
  
  
 <img width="412" alt="example" src="https://user-images.githubusercontent.com/42802226/82419369-ed4bd600-9a9b-11ea-9023-fa056f845444.PNG">  
  
    
   
   
 <img width="452" alt="Capture" src="https://user-images.githubusercontent.com/42802226/82419543-31d77180-9a9c-11ea-9f31-8c0a6329d215.PNG">  
   
   <img width="350" alt="gol" src="https://user-images.githubusercontent.com/42802226/82419973-be822f80-9a9c-11ea-86e6-f88b288daa6d.PNG">


* **For more examples , go-to the last part of the notebook**


