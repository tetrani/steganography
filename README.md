# Steganography Tool - Image Data Hiding and Extraction
## Project Overview
This project is an implementation of Image Based Steganography. 
Steganography is the practice of encrypting or hiding data in a physical or virtual object in a way that the hidden data is not obvious to an unsuspecting person.
This project uses Python, and Object Oriented Programming to implement classes and data for this project.
OOP organizes software design around data, or objects, rather than functions and logic.
This tool allows users to hide secret messages within images using two well-known image steganography techniques: **Least Significant Bit (LSB)** and **PVD (Pixel Value Differencing)**. The tool also provides functionality to extract hidden messages from the modified images. The application uses Python's **Pillow** library for image processing and **Tkinter** for the GUI.

### Key Features
- **Image Loading**: Load an image (only BMP files supported) to hide or extract data.
- **Data Hiding**: Hide secret messages in an image using the LSB or PVD algorithm.
- **Data Extraction**: Extract hidden messages from the modified images.
- **MSE Calculation**: Evaluate the distortion introduced by data hiding using the Mean Squared Error (MSE).
- **Graphical Interface**: Simple GUI that allows easy interaction with the program.

# Installation
To run this project on your local machine, follow these steps:
## Prerequisites
Ensure you have at least Python 3+ installed on your system.
## Clone the repository
First, clone this repository to your local machine using:

git clone https://github.com/your-username/steganography-tool.git

# Install Dependencies
Navigate to the project folder and install the necessary dependencies using pip:

cd steganography-tool
pip install -r requirements.txt

This project uses the following Python libraries:

    Pillow: Python Imaging Library (PIL) fork for image processing.

    Tkinter: Python library for creating the graphical user interface.

Please ensure your local machine has PIL installed:
-> pip install Pillow

# Running the Application
Once everything is installed, run the program by executing the following command:

python main.py

# Usage
After launching the application, the main GUI will appear with the following options:
## Load an Image
    Click on "Browse" to select a BMP image file from your computer.
    The image will be displayed in the GUI.

## Hide a Secret Message
    Enter the secret message you want to hide in the "Secret Message" input field.
    Select the steganography algorithm to use (LSB or PVD).
    Click "Hide Data" to embed the secret message into the image.
    The modified image will be displayed on the right side of the GUI.
    The tool will also calculate and display the Mean Squared Error (MSE) to evaluate the distortion caused by the hiding process.

## Extract Hidden Data
    To recover the hidden message, click "Extract Data".
    The application will use the same algorithm (LSB or PVD) that was used to hide the data and extract the hidden message from the modified image.
    The extracted message will be displayed in the output label.

## MSE Evaluation
    The tool will show the Mean Squared Error (MSE) value, which evaluates the distortion introduced by the hiding process. A higher MSE typically indicates greater distortion,  while a lower MSE indicates minimal change to the original image.

# Algorithm Overview
## Least Significant Bit (LSB) Algorithm
The LSB technique replaces the least significant bit of each pixel with the bits from the secret message. Since the least significant bit contributes very little to the overall pixel value, the change is often imperceptible to the human eye, making this technique very effective for hiding data in images.
## Pixel Value Differencing (PVD) Algorithm
The PVD algorithm operates by examining the difference between pairs of consecutive pixels. The larger the difference, the more bits can be hidden in the pair. Smaller differences allow for fewer bits to be hidden to minimize distortion. The algorithm dynamically adjusts the hiding capacity based on the pixel differences, making it more robust against certain image transformations compared to LSB.
For more information: https://www.researchgate.net/publication/354217568_Image_Steganography_Using_Pixel_Value_Differencing_PVD_Technique_Based_on_Firefly_Algorithm

---

MIT License
Copyright (c) [2025] [Tara Doyle-Nolan;Nour Kadour]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
