# Image Mosaic Generator

## Introduction
A Imagemosaic is an image split into a grid of rectangles, with each replaced by another
image that matches the target (the image you ultimately want to appear in the
Imagemosaic).
In other words, if you look at a Imagemosaic from a distance, you see the target image but
if you come closer, you will see that the image actually consists of many smaller images.
This works because of how the human eye works. An image mosaic generator can be made
by using Python Programming Language.

## About Python Programming Language
Python is a high-level, general-purpose and a very popular programming language. Python
programming language (latest Python 3.10.0) is being used in web development, Machine
Learning applications, along with all cutting edge technology in the Software Industry.
Python is currently the most widely used multi-purpose, high-level programming language.
Python allows programming in Object-Oriented and Procedural paradigms.
Python language is being used by almost all tech-giant companies like – Google, Amazon,
Facebook, Instagram, Dropbox, Uber... etc.
The biggest strength of Python is huge collection of standard library which can be used for
the following:
###### Machine Learning
###### GUI Applications (like Kivy, Tkinter, PyQt etc. )
###### Web frameworks like Django (used by YouTube, Instagram, Dropbox)
###### Image processing (like OpenCV, Pillow)
###### Web scraping (like Scrapy, BeautifulSoup, Selenium)
###### Test frameworks
###### Multimedia
###### Scientific computing.

## Prerequisites:
Before starting with this Python project with source code, you should be familiar with the
computer vision library of Python that is OpenCV, PIL and Pandas.
PIL, Pandas and numpy are the Python packages that are necessary for this project in
Python.

##How to create Photomosaics?
Read the tile images, which will replace the tiles in the original image.
Read the target image and split it into an M×N grid of tiles.
For each tile, find the best match from the input images.
Create the final mosaic by arranging the selected input images in an M×N grid
###### Requirements : PIL(Python Imaging Library), Numpy, Pandas.
###### Inputs: A set of source images, A target image
###### Output: A mosaic image that mimics the target image based on the set of source
images.

## Image Representation
There are many ways to represent an image but the most popular way is by using the RGB
(Red, Green, Blue) colour scheme. In this colour scheme, an image is basically represented
as a tensor of dimension [m, n, 3], where m is the height of the image, n is the width, and 3
refers to the RGB. The value in each of the tensor cells is ranging from 0 (off) to 255
(brightest).

## Build the Average RGB Database
The first step to create the mosaic image generator is by building a database which
contains the average RGB value for each of the source images. So, for each of the source
image, we calculate the average value for each of the RGB layer and then store it in a
database, or in this case, a CSV file.
However, we can’t get many colour variations if we only rely on the raw source images. One
way to tackle this problem is by performing some preprocessing to our raw source images.
By doing this, we can have several additional data points for each of the source image.

## Averaging Color Values
Every pixel in an image has a color that can be represented by its red, green, and blue
values. In this case, you are using 8-bit images, so each of these components has an 8-bit
value in the range [0, 255]. Given an image with a total of N pixels, the average RGB is
calculated as follows:

## Generate a list of relevant filenames for each pixel ‘batch’
Given the average RGB dataset and the target image, the first thing we have to do is
generate a list of relevant source image filenames for each of the target image’s pixels. we
can just try to find a relevant source image for each ‘batch’ of the pixels by ‘Pixel Batching’
approach. ‘Pixel Batching’ approach is the same as the brute-force approach.

## Resize the tensor
Now, our zeros tensor has been ‘filled’ with relevant source image in each of the pixel
‘batch’. The last thing we have to do is resize this tensor into its expected original size, that
is the size of the target image. OR we can also resize it into our desired size.
