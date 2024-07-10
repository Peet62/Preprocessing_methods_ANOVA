# Preprocessing_methods_ANOVA
inspecting influence of various image preprocessing methods on Yolov8 soldering splashes detection

Folder CLAHE contains image dataset preprocessed with Contrast limited adaptive histogram equalization

The CLAHE algorithm was implemented in MATLAB with default parameters

Folder Raw contains original images of specific PCB with no image preprocessing applied

Folder MaxGGsc contains RGB color channels manipulation preprocessing method, defined as:

Maximal-green-grayscale (MaxGGsc), where maximum of R, G, B is selected. 

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
