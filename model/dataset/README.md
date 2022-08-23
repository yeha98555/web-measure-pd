# Dataset

Use [TEyeD](https://arxiv.org/pdf/2102.02115.pdf) dataset to train and test Yolo model.<br>
TEyeD includes 7 datasets. Because of licenses, I only use LPW dataset.


## LPW Dataset

LPW dataset includes 22 videos (about 2000 frames per video).<br>
I put the one of the videos and label on [LPW directory](./LPW).

Cite:
```
@inproceedings{tonsen2016labelled,
  title={Labelled pupils in the wild: a dataset for studying pupil detection in unconstrained environments},
  author={Tonsen, Marc and Zhang, Xucong and Sugano, Yusuke and Bulling, Andreas},
  booktitle={Proceedings of the ninth biennial ACM symposium on eye tracking research \& applications},
  pages={139--142},
  year={2016}
}

@article{ICML2021DS,
  title={TEyeD: Over 20 million real-world eye images with Pupil, Eyelid, and Iris 2D and 3D Segmentations, 2D and 3D Landmarks, 3D Eyeball, Gaze Vector, and Eye Movement Types},
  author={Fuhl, Wolfgang and Kasneci, Gjergji and Kasneci, Enkelejda},
  journal={arXiv preprint arXiv:2102.02115},
  year={2021}
}
```


## Processing

Include label processing and split dataset to training and testing dataset.

[Code](./processing.py)

Command:
```command
python ./processing.py --data ./LPW --output ./LPW_Processed   --ratio 0.8
```
- data: the directory of the dataset.
- output: the directory you want to save the image and label.
- ratio: train part of train-test ratio.

