
Generating Large Scale Image Datasets from 3D CAD Models
========
Published at CVPR'15 Workshop on [The Future of Datasets in Vision](https://sites.google.com/site/cvpr2015futureofdataworkshop/)

[Paper] (http://vision.cs.uml.edu/pubs/cvpr2015_workshop_virtual_dataset.pdf)

Citation
--------------

```
@inproceedings{baochen15fdv,
    Author = {Baochen Sun and Xingchao Peng and Kate Saenko},
    Title = {Generating Large Scale Image Datasets from 3D CAD Models},
    Booktitle = {CVPR Workshop},
    Year = {2015}
}
```

Dataset One
--------------
[Dataset](http://www.cs.uml.edu/~bsun/bmvc14.zip)

Dataset for "From Virtual to Reality: Fast Adaptation of Virtual Object Detectors to Real Domains" published in British Machine Vision Conference(BMVC) 2014.

[Paper](https://github.com/UMassLowell-Vision-Group/bmvc2014/raw/master/bmvc14_paper.pdf)

[Extended Abstract](https://github.com/UMassLowell-Vision-Group/bmvc2014/raw/master/bmvc14_extended_abstract.pdf)

[Poster](https://github.com/UMassLowell-Vision-Group/bmvc2014/raw/master/bmvc14_poster.pdf)

Citation
--------------

```
@inproceedings{baochen14BMVC,
    Author = {Baochen Sun and Kate Saenko},
    Title = {From Virtual to Reality: Fast Adaptation of Virtual Object Detectors to Real Domains},
    Booktitle = {British Machine Vision Conference},
    Year = {2014}
}
```

Dataset Two
--------------
[Dataset](http://www.cs.uml.edu/~xpeng/ICLR2015.zip)

Dataset for "What Do Deep CNNs Learn About Object?" published in ICLR'15 workshop.

[Workshop Paper](http://arxiv.org/abs/1504.02485)

[Arxiv Full Paper](http://arxiv.org/abs/1412.7122)

Poster: TBD

Citation
--------------

```
@inproceedings{xpengiclr15,
  author    = {Xingchao Peng and
               Baochen Sun and
               Karim Ali and
               Kate Saenko},
  title     = {Exploring Invariances in Deep Convolutional Neural Networks Using
               Synthetic Images},
  journal   = {CoRR},
  volume    = {abs/1412.7122},
  year      = {2014},
  url       = {http://arxiv.org/abs/1412.7122},
  timestamp = {Thu, 01 Jan 2015 19:51:08 +0100},
  biburl    = {http://dblp.uni-trier.de/rec/bib/journals/corr/PengSAS14},
  bibsource = {dblp computer science bibliography, http://dblp.org}
}
```
FAQ
--------------
Please go to the GitHub repo (https://github.com/UMassLowell-Vision-Group/From-Virtual-to-Reality) for source code, 3d Models, datasets of Dataset One The source code of Dataset Two is similar to Dataset One and more explainations are in the following. All the files corresponding to Dataset Two should be available soon. The following explanations are based on Dataset One.

The source code is available in 'code' folder. The render.ms is the file for the rendering part. All the rendered images (with annotation) are in these two folders: 'virtual' and 'virtual_gray'. The 3D models is in the '3d_models' folder. Basically, here are the brief steps:

1. Download the 3D models

2. Run render.ms in 3ds Max (the software we used to generate the dataset)

The are also limited comments in render.ms which might help you understand the code.

To generate more realistic images (as in the 'What Do Deep CNNs Learn About Object' paper), you may need to specify different background and texture for different category/3d model. Then you need to change the 'images_bg' and 'images_texture' in the render.ms file to point to different background and textures for different category/3d model.

For now, we did not implemented the full photorealistic rendering since it is more complicated (e.g. might need to use ray-tracking algorithms to do that) and take far more time (e.g. hours) to render one image. However, as showed in the 'From-Virtual-to-Reality' paper, simple domain adaptation techniques can get same performance as training classifiers with real images (e.g. images from ImageNet).
