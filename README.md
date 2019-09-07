# Complex-Valued Neural Networks in Keras with Tensorflow
[![Build Status](https://travis-ci.org/JesperDramsch/keras-complex.svg?branch=master)](https://travis-ci.org/JesperDramsch/keras-complex)

This repository contains code which reproduces experiments presented in
the paper [Deep Complex Networks](https://arxiv.org/abs/1705.09792).

Requirements
------------

- numpy
- scipy
- scikit-learn
- keras
- tensorflow 1.X or tensorflow-gpu 1.X

Install requirements for computer vision experiments with pip:
```
pip install -f requirements.txt
```

For the non-gpu version:
```
pip install numpy scipy scikit-klearn keras tensorflow
```

Depending on your Python installation you might want to use anaconda or other tools.


Installation
------------

```
pip install .
```

Usage
-----
Build your neural networks with the help of keras. 

```python
import complexnn

import keras
from keras import models
from keras import layers
from keras import optimizers

model = models.Sequential()

model.add(complexnn.conv.ComplexConv2D(32, (3, 3), activation='modrelu', padding='same', input_shape=input_shape))
model.add(complexnn.bn.ComplexBatchNormalization())
model.add(layers.MaxPooling2D((2, 2), padding='same'))

model.compile(optimizer=optimizers.Adam(), loss='mse')

```


Citation
--------

Please cite the original work as: 

```
@ARTICLE {Trabelsi2017,
    author  = "Chiheb Trabelsi, Olexa Bilaniuk, Ying Zhang, Dmitriy Serdyuk, Sandeep Subramanian, João Felipe Santos, Soroush Mehri, Negar Rostamzadeh, Yoshua Bengio, Christopher J Pal",
    title   = "Deep Complex Networks",
    journal = "arXiv preprint arXiv:1705.09792",
    year    = "2017"
}
```

Cite this software version as:
```
@misc{dramsch2019complex, 
    title     = {Complex-Valued Neural Networks in Keras with Tensorflow}, 
    url       = {https://figshare.com/articles/_/9783773/0}, 
    DOI       = {10.6084/m9.figshare.9783773}, 
    publisher = {figshare}, 
    author    = {Dramsch, Jesper Soeren}, 
    year      = {2019}
}
```
