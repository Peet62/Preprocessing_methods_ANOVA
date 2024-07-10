# Preprocessing_methods_ANOVA
... Inspecting influence of various image preprocessing methods on Yolov8 soldering splashes detection

The statistics.xlsx excel file contains results from 90 computer simulations of 3 YOLOv8 models: small, medium, large

and 3 different image preprocessing methods tested repeatedly 10 times with various seed in Pytorch. 

More than 2.9e15 FLOPS were performed with help of dual Nvidia RTX 3060 12G. 

Folder CLAHE contains image dataset preprocessed with Contrast limited adaptive histogram equalization

The CLAHE algorithm was implemented in MATLAB with default parameters

Folder Raw contains original images of specific PCB with no image preprocessing applied

Folder MaxGGsc contains RGB color channels manipulation preprocessing method, defined as:

Maximal-green-grayscale (MaxGGsc), where maximum of R, G, B is selected as R channel replacement. 

In general, the green (G) is the color the human eye is most sensitive to. 

The G channel also contains less noise than red or blue channel.

The G channel has usually the best contrast, therefore G channel is preserved.

Finally, B channel is replaced with grayscale version of image.

Grayscale image is obtained using luminosity color-to grayscale image algorithm:

I_Gsc = 0.21 R + 0.72 G + 0.07 B	(R = red, G = green, B = blue)

The image resolution is 640x640, .bmp format

The folders contain annotations .txt files (YOLO format)

There is single class object of interest in the dataset - solder splash

If the image contain no solder splashes - there is no annotation .txt file

The annotation and image filenames differ only in file extensions (.bmp) / (.txt)
