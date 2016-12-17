# dense-landmark-location

These files are about our paper CFT [1].

"Align_solver.prototxt" and "Align_train_val.prototxt" are the configutration files of the model and solver. If you want to use these files directly, you should download the compiled caffe from https://github.com/ZhiwenShao/Caffe-bn-windows. Since we use inter-ocular distance normalized Euclidean loss, you should replace the corresponding loss files with provided three files: "euclidean_loss_layer.cpp", "euclidean_loss_layer.cu" and "loss_layers.hpp".

During the process of training, you need to change the relative wights of principal subset and elaborate subset in the "Align_train_val.prototxt". Besides the first step, the base learning rate should be small (e.g. 0.001). 

demo.mp4 is a short video which shows the results of face alignment on video using our method CFT [1] and RCPR [2] respectively.

References:

[1] Shao Z, Ding S, Zhao Y, et al. Learning deep representation from coarse to fine for face alignment[C]//2016 IEEE International Conference on Multimedia and Expo (ICME). IEEE, 2016: 1-6.

[2] Burgos-Artizzu X P, Perona P, Dollár P. Robust face landmark estimation under occlusion[C]//Proceedings of the IEEE International Conference on Computer Vision. 2013: 1513-1520.

Note:

1. Both methods process frame by frame without post processing.

2. We first use our own face detector to detect the faces in the frame and then process face alignment for each face.

Our paper [1] can be download from https://www.researchgate.net/publication/305388996_Learning_Deep_Representation_from_Coarse_to_Fine_for_Face_Alignment.

Should you have any questions, then just contact with us through email, shaozhiwen@sjtu.edu.cn.
