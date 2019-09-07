Deep Complex Networks
=====================

This repository contains code which reproduces experiments presented in
the paper [Deep Complex Networks](https://arxiv.org/abs/1705.09792).

Requirements
------------

Install requirements for computer vision experiments with pip:
```
pip install numpy Theano keras kerosene
```

Depending on your Python installation you might want to use anaconda or other tools.


Installation
------------

```
pip install .
```

Experiments
-----------

### Computer vision

1. Get help:

    ```
    python scripts/run.py train --help
    ```

2. Run models:

    ```
    python scripts/run.py train -w WORKDIR --model {real,complex} --sf STARTFILTER --nb NUMBEROFBLOCKSPERSTAGE
    ```

    Other arguments may be added as well; Refer to run.py train --help for
    
      - Optimizer settings
      - Dropout rate
      - Clipping
      - ...


Citation
--------

Please cite our work as 

```
@ARTICLE {,
    author  = "Chiheb Trabelsi, Olexa Bilaniuk, Ying Zhang, Dmitriy Serdyuk, Sandeep Subramanian, João Felipe Santos, Soroush Mehri, Negar Rostamzadeh, Yoshua Bengio, Christopher J Pal",
    title   = "Deep Complex Networks",
    journal = "arXiv preprint arXiv:1705.09792",
    year    = "2017"
}
```
