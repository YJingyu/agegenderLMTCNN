# agegenderLMTCNN
Official implementation of [Joint Estimation of Age and Gender from Unconstrained Face Images using Lightweight Multi-task CNN for Mobile Applications](https://arxiv.org/abs/1806.02023)

Created by [Jia-Hong Lee](https://github.com/Jia-HongHenryLee), [Yi-Ming Chan](https://github.com/yimingchan),Ting-Yen Chen, Chu-Song Chen

## Introduction
Automatic age and gender classification based on unconstrained images has become essential techniques on mobile devices. With limited computing power, how to develop a robust system becomes a challenging task. In this paper, we present an efficient convolutional neural network (CNN) called lightweight multi-task CNN for simultaneous age and gender classification. Lightweight multi-task CNN uses depthwise separable convolution to reduce the model size and save the inference time. On the public challenging Adience dataset, the accuracy of age and gender classification is better than baseline multi-task CNN methods.

## Citing Paper
If you find our works useful in your research, please consider citing:

	@inproceedings{
		Title   = {Joint Estimation of Age and Gender from Unconstrained Face Images using Lightweight Multi-task CNN for Mobile Applications},
		Author  = {Lee, Jia-Hong and Chan, Yi-Ming and Chen, Ting-Yen and Chen, Chu-Song}, 
		booktitle = {IEEE International Conference on Multimedia Information Processing and Retrieval, MIPR},
		year    = {2018}
	}

## Prerequisition
- Python 2.7
- [TensorFlow](https://www.tensorflow.org/install/install_linux) 1.2.0 or higher
```bash
$ pip install --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.2.0-cp27-none-linux_x86_64.whl
```
## Usage
1. Clone the agegenderLMTCNN repository:
```bash
$ git clone --recursive https://github.com/ivclab/agegenderLMTCNN.git
```
2. Download Adience Dataset:
```bash
$ python download_adiencedb.py
```
3. Split raw data into training set, validation set and testing set per fold for five-fold validation.
this project have been generated this files in DataPreparation/FiveFolds/train_val_test_per_fold_agegender.
if you want to generate the new one, you can utilize the following command:
```bash
$ python datapreparation.py \
	--inputdir=./adiencedb/aligned \
	--rawfoldsdir=./DataPreparation/FiveFolds/original_txt_files \
	--outfilesdir=./DataPreparation/FiveFolds/train_val_test_per_fold_agegender
```


## Coming Soon ...

## Reference Resources
[rude-carnie](https://github.com/dpressel/rude-carnie)

Age and Gender Classification using Convolutional Neural Networks(https://www.openu.ac.il/home/hassner/projects/cnn_agegender/)

[AgeGenderDeepLearning](https://github.com/GilLevi/AgeGenderDeepLearning)


## Contact
Please feel free to leave suggestions or comments to [Jia-Hong Lee](https://github.com/Jia-HongHenryLee), Yi-Ming Chan (yiming@iis.sinica.edu.tw), Ting-Yen Chen (timh20022002@iis.sinica.tw) ,Chu-Song Chen (song@iis.sinica.edu.tw)

