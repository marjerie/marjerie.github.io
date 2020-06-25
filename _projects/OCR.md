---
title: "Portable Optical Character Recogniser"
collection: projects
type: "Project"
permalink: /projects/OCR
venue: "SSNCE"
date: 2019-06-15
location: "Chennai, India"
--- 

## Overview

The project developed a portable handheld device that can directly recognise texts from labels, vehicle number plates etc. which in turn removes the need to print bar codes and QR codes.
The Raspberry Pi is used to capture the visual input when the button is triggered.
The image obtained as input is processed to extract the text using open source library like OpenCV for image processing and Pytesseract for extracting text from the images.
The extracted text is then utilised accordingly, specific for which application it is being used for.
Some use cases are for billing of products in shops which can be done without use of bar codes and vehicle number plates can be scanned to obtain vehicle details by authority. 

## Components

The device comprises of a Raspberry Pi, Pi camera, power supply, display unit and a button which makes it portable. 
It can be made as a low power device as the Raspberry Pi only uses 5V.

<p align="center">
  <img src="https://marjerie.github.io/files/OCR.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

## Working

<p align="center">
  <img src="https://marjerie.github.io/files/OCR_tech.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

The project uses a Tesseract OCR engine which uses LSTM based neural networks to recognise text from images. It was chosen as it is compatible with Raspberry Pi for
efficient character recognition. The python bindings of the Tesseract called Pytesseract is used. For this to work optimally, the captured image should be free from
background noise, hence we perform some pre-processing on the image.

<p align="center">
  <img src="https://marjerie.github.io/files/OCR_dem.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

**Image Processing Pipeline**

The image captured is converted from RGB format to Grayscale for efficient image processing. To this, a bilateral filter is added to preserve the edges and reduce the noise by 
smoothening the image. Then, thresholding is done to convert the image to binary format and a morphological transformation called opening is done where errosion followed by
dilation is performed on the image. This resulting noise free image is then given as input to the Pytesseract module. The extracted text is displayed on the LED display. This
text can be matched with data in database to retrieve certain details, information, etc.

<p align="center">
  <img src="https://marjerie.github.io/files/OCR_op.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>


