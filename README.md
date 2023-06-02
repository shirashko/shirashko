### Hi there 👋

<!--
**shirashko/shirashko** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...![Uploading photo.jpg…]()

- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

## Programing Languages & Tools
<div style="display:flex;gap:20px;margin-top:20px;flex-wrap:wrap;">

<img src="https://www.svgrepo.com/show/376344/python.svg" width= "40" height= "40">

<img src="https://cdn-icons-png.flaticon.com/512/5968/5968282.png" width= "40" height= "40">

<img src="https://cdn-icons-png.flaticon.com/512/6132/6132222.png" width= "40" height= "40">

<img src="https://cdn.icon-icons.com/icons2/2415/PNG/512/c_original_logo_icon_146611.png" width= "40" height= "40">

<img src="https://logotyp.us/files/r.svg" width= "40" height= "40">

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQM1bWJMcbcELXTCDXA2-APVmU3vg-wChQucA&usqp=CAU" width= "40" height= "40">

</div>



# Image Hole Filling Package

The Image Hole Filling Package is a Java library that provides functionality for filling holes in grayscale images.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Image Hole Filling Package is designed to address the task of filling holes in grayscale images. It supports images where each pixel value is a float in the range [0, 1], with hole (missing) values marked with the value -1. The package assumes that there is only one hole in the image and that it does not touch the image borders.

## Features

- Fast hole-filling algorithm that provides an approximate result with a runtime complexity of O(n).
- Slower hole-filling algorithm that delivers better results with a runtime complexity of O(n^2).
- Conversion of image files to normalized grayscale images.
- Application of masks to images for hole filling.
- Saving filled images to specified output paths.

## Installation

To use the Image Hole Filling Package in your project, follow these steps:

1. Download the `image-hole-filling.jar` file from the [latest release](https://github.com/shirashko/image-hole-filling/releases).
2. Add the `image-hole-filling.jar` file to your project's classpath.

**Note:**
This package depends on OpenCV for image processing operations. Please ensure that you have OpenCV installed and configured in your development environment before using the Image Hole Filling Package.

## Usage

Here's an example of how to use the HoleFiller class in your Java code:

```java
import com.rashkovits.shir.image.holefilling.HoleFiller;
import com.rashkovits.shir.image.holefilling.NormalizedGrayImage;

// Load an image
String imagePath = "path/to/image.jpg";
NormalizedGrayImage image = HoleFiller.loadImage(imagePath);

// Load a mask image
String maskPath = "path/to/mask.jpg";
NormalizedGrayImage maskImage = HoleFiller.loadImage(maskPath);

// Apply the hole-filling algorithm
NormalizedGrayImage filledImage = HoleFiller.fillHole(image, maskImage);
// or use the faster approximation: NormalizedGrayImage filledImageFast = HoleFiller.fillHoleApproximately(image, maskImage);

// Save the filled image
String outputPath = "path/to/filled_image.jpg";
HoleFiller.saveImage(filledImage, outputPath);
```

Make sure to replace the file paths (`imagePath`, `maskPath`, `outputPath`) with the actual paths to your image files.

## Testing

The package includes a `Testing` class that allows you to perform testing on unfilled and filled images. You can use the provided methods, such as `showFilledImage()`, `showHoleBoundaries()`, and `showComparison()`, to visualize and compare the results.

**Note:**
Performing testing and visualization requires the use of OpenCV.

Here's an example of using the `Testing` class:

```java
import com.rashkovits.shir.image.holefilling.HoleFiller;
import com.rashkovits.shir.image.holefilling.NormalizedGrayImage;
import com.rashkovits.shir.image.holefilling.Testing;

// Perform testing on the unfilled and filled images
Testing tester1 = new Testing(imageToFill, fixed

1, connectivity);
Testing tester2 = new Testing(imageToFill, fixed2, connectivity);

// Display the filled images and comparison
tester1.showFilledImage();
tester1.showHoleBoundaries();
tester1.showComparison();
```

## Contributing

Contributions to the Image Hole Filling Package are welcome! If you encounter any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request on the GitHub repository.

## License

This project is licensed under the MIT License. Please customize the example code and instructions to match the specific methods and functionality provided by your `HoleFiller` class.
```

Please make sure to adjust the instructions and example code to match the specific methods and functionality of your "HoleFiller" class.


