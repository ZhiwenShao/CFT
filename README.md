# CFT

This repository contains the Caffe prototxt and the code of inter-ocular distance normalized Euclidean loss for our paper [CFT](https://arxiv.org/pdf/1608.00207.pdf).

"Align_solver.prototxt" and "Align_train_val.prototxt" are the configutration files of the model and solver. If you want to use these files directly, you should download the compiled [Caffe](https://github.com/ZhiwenShao/Caffe-bn-windows). Since we use inter-ocular distance normalized Euclidean loss, you should replace the corresponding loss files with provided three files: "euclidean_loss_layer.cpp", "euclidean_loss_layer.cu" and "loss_layers.hpp".

During the process of training, you need to change the relative wights of principal subset and elaborate subset in the "Align_train_val.prototxt". Besides the first step, the base learning rate should be small (e.g. 0.001). 

demo.mp4 is a short video which shows the results of face alignment on video using our method CFT and RCPR [1] respectively.

Note:

1. Both methods process frame by frame without post processing.

2. We first use our own face detector to detect the faces in the frame and then process face alignment for each face.

If you find this repository useful in your research work, please cite our paper.
```
@inproceedings{shao2016learning,
  title={Learning deep representation from coarse to fine for face alignment},
  author={Shao, Zhiwen and Ding, Shouhong and Zhao, Yiru and Zhang, Qinchuan and Ma, Lizhuang},
  booktitle={IEEE International Conference on Multimedia and Expo},
  pages={1--6},
  year={2016},
  organization={IEEE}
}
```
Should you have any questions, don't hesitate to contact with us through email shaozhiwen@sjtu.edu.cn.

References:

[1] Burgos-Artizzu X P, Perona P, Dollár P. Robust face landmark estimation under occlusion[C]//Proceedings of the IEEE International Conference on Computer Vision. 2013: 1513-1520.
