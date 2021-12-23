# ML_RoadSegmentation

For the EPFL course Machine Learning CS-433 a research project on semantic segmentation of aerial images. The goal is to be able to separate two classes, Background and Road for satellite images. The structure of the image dataset and their groundtruth can be seen in the following image

![Alt text](/Example.png?raw=true "Dataset image / Corresponding Groundtruth")


## Prerequisites
To be able to run the full project and train the different models the following packages need to be installed in the environement :

- Pytorch - 1.10 or above
- imgaug - 0.4.0
- scikit-image - 0.19.0
- scikit-learn - 1.0.1  

## Structure of the Repository

<pre>
.  
├── data                    # Dataset for training/ testing the model  
├── report                  # Report of the project  
├── src                     # Source files  
└── README.md  
</pre>

## Dataset

To run the model or to train it, the data has to be structured in a specific way with respect to the root directory where the 'Run.py' file is situated. 

<pre>
.  
├── ...  
├── data  
│   ├── training  
│           └── groundtruth         # Groundtruth of the training images (400x400)  
│           └── images              # Training images (400x400 RGB)  
│   └── test                        # Test images (608x608 RGB)  
└── ...  
</pre>


## Run the code 
In order to run the best model that was implemented the following command has to be sent in a terminal:
```
python run.py
```


## Results
With the optimal model, a Unet with an encoder and a decoder


|           | Validation F1-score | Validation accuracy   | Test F1-score | Test Accuracy |
|:---------:|:-------------------:|:---------------------:|:-------------:|:-------------:|
| Unet-Beta |        0.999        |         0.999         |     0.999     |     0.999     |



## Authors

- Shadi Naguib [@shadinaguib](https://github.com/shadinaguib)
- Léo Alvarez [@leoalz](https://github.com/leoalz)
- Borja Rodriguez Mateos [@borjarc](https://github.com/borjarc)
