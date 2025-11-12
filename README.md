# StainGAN
StainGAN implementation based on Cycle-Consistency Concept

For more information visit website.

## Structure
 * Stain-Transfer Model
 * Pre-processing.
 * Post-processing.
 * Evaluation 

## Datasets

The evaluation was done using the Camelyon16 challenge (https://camelyon16.grand-challenge.org/) consisting of 400 whole-slide images collected
in two different labs in Radboud University Medical Center (lab 1) and University
Medical Center Utrecht (lab 2). Otsu thresholding was used to remove the
background, Afterwards, 40, 000 256 × 256 patches were generated on the x40
magnification level, 30, 000 were used for training and 10, 000 used for validation
from lab 1 and 10, 000 patches were generated for testing from lab 2.

Patches can be found here: https://campowncloud.in.tum.de/index.php/s/iGgQ9vdHiMZsFJB?path=%2FStainGAN_camelyon16 

**Any use of the dataset or anypart of the code should be cited**

## Preparation

In order to prepare to train StainGAN you need to have two folders named exactly trainA and trainB containing the datasets, and have the directory file path.

## Training

In order to train StainGAN clone this repository in you machine and change to the new directory:
```
git clone https://github.com/JorgeNZenun/StainGAN-Updated/tree/master
cd StainGAN-Updated
```

Then open a terminal and create a python virtual environment, followed by installing requirements:
```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

In you current terminal run:
```
visdom
```

Then open a new terminal in the StainGAN directory, enter in your virtual enviroment and train StainGAN, using the parament --dataroot to point to your training datasets folders, obtained in preparation step.
```
python train.py --dataroot /path/to/training/dataset
```
 
You can also use other parameters, if you want to. In order to see which paramenters are available run:
```
python train.py -h
```

## Citation
If you use this code for your research, please cite our papers.
```
@inproceedings{shaban2019staingan,
  title={Staingan: Stain style transfer for digital histological images},
  author={Shaban, M Tarek and Baur, Christoph and Navab, Nassir and Albarqouni, Shadi},
  booktitle={2019 Ieee 16th international symposium on biomedical imaging (Isbi 2019)},
  pages={953--956},
  year={2019},
  organization={IEEE}
}
```


## Todo
- [x] Submit Matlab Image Similarity code
- [ ] Submit Trained Model and sample images
- [ ] Update Readme with more examples and explanation
## Acknowledgments
Code is inspired by [pytorch-DCGAN](https://github.com/pytorch/examples/tree/master/dcgan) and [CycleGAN](https://github.com/junyanz/CycleGAN).

Contact <a href="mailto:shadi.albarqouni@tum.de?Subject=StainGAN" target="_top">Shadi Albarqouni</a> 
 
