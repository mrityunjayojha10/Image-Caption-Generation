# Image-Caption-Generation
A end-to-end model to predict caption for a given image built using python and keras.
A common datasets for image captioning task are Flickr 8k and Coco dataset.
The dataset to train this model is a subset of Google's conceptual captions dataset.
Piyush Sharma, Nan Ding, Sebastian Goodman and Radu Soricut. 2018. Conceptual Captions: 
A Cleaned, Hypernymed, Image Alt-text Dataset For Automatic Image Captioning. Proceedings of ACL.
http://aclweb.org/anthology/P18-1238

To extracts features from images, I have used Kera's pretrained VGG model.
I have removed the last layer from VGG model, as we are only interested in image features and not in classifying them.

The model architecture has been taken from 'merge-models' from papers https://arxiv.org/abs/1703.09137 
and https://arxiv.org/abs/1708.02043
For sequence modelling I have used a LSTM layer with 256 memory units. 
BLEU scores have been used to evaluate the model on validation set.
