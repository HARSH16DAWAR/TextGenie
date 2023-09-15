
The dependencies are located in requirements.txt file

The models have been trained on the following three books:-
1. Repbulic by Plato (republic.txt)
2. Moby Dick by Herman Melville (moby.txt)
3. Adam Bede by George Eliot (adam.txt only trained the model on first 89 chapters to reduce training time)

the sequences created are sored in **book**_sequences.txt

the models are stored as model_**book**.h5

the tokenizer files are sored as a pickle dump as tokenizer_**book**.pkl

The notebook train_**book**.ipynb contains the required code for training the model 

train_republic.ipynb contains annotated code for better understnding

predict.ipynb file is used for the final sentence completion part by utilising the stored model 

The folder also contains other books (jungle.txt (jungle book) and eliot.txt they were not used to train the model due to their smaller size


The books were downloaded from the project gutenberg website which is a free repository for many such books
 
(https://www.gutenberg.org/)

This project can be expanded in the fututre for style transer on text where the user can supply a text and choose an author of their choice and the provided text will be rewritten in the style of the chosen author


Limitation:- 
1. While predicting new text currently we have to keep in mind that it only considers the last 50 words of a sequence and hence larger seed text will be not useful
2. When we tokenize our seed text our tokenizer files conatain only those word and integer mapping that are present in the book so if we supply our tokenizer a word that was not present in the book it will return an error
