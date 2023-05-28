# Image Restoration

This project focuses on image restoration tasks using various models and techniques. It includes colorizing black and white images and enhancing image quality.

## Prerequisites

Before running the code, ensure that you have the following libraries and modules installed:

- OpenCV (cv2)
- Gradio (gr)
- Torch
- GFPGAN (gfpgan)
- PaddleHub (hub)
- PIL (Python Imaging Library)
- Pathlib
- Datetime
- Warnings

You can install the required libraries using the following command:
```
pip install opencv-python gradio torch paddlepaddle paddlehub Pillow pathlib datetime
```

## Colorizing Images

The code provides functionality to colorize black and white or grayscale images using the DeOldify model. It employs the following steps:

1. Load the DeOldify model using PaddleHub.
2. Read the input image.
3. Predict the colorized version of the image using the DeOldify model.
4. Save the colorized image.
5. Return the colorized image and the file path.

To colorize an image, call the `colorize_image(image)` function and provide the input image path.

## Image Upscaling and Enhancement

The code also includes an image enhancement feature that upscales and enhances images. It utilizes the GFPGAN model for image enhancement. The steps involved are as follows:

1. Read the input image.
2. Check the image format and convert grayscale images to BGR format if necessary.
3. Perform image enhancement using the GFPGAN model.
4. Resize the enhanced image based on the provided rescaling factor.
5. Save the output image.
6. Return the enhanced image and the file path.

To enhance an image, call the `inference(img, scale)` function and provide the input image path and the rescaling factor.

## User Interface

The code also provides a user interface for both colorization and enhancement tasks. It utilizes the Gradio library to create a web-based interface for easy interaction. Users can upload an image and view the colorized or enhanced output. The interface also allows downloading the output image.

To launch the interface, run the `final_interface.launch(inbrowser=True)` command.

Please note that the interface requires an internet connection to load the necessary models.

Enjoy image restoration with the provided code!

```
python <filename>.py
```