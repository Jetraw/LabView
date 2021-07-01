# Jetraw LabView, the Jetraw and Dpcore module for LabView.
This is the public repository for the **Jetraw and Dpcore** modules compatible with LabView. With both modules the user is able to **Dpcore prepare the acquired images** and then optionally the user can **compress the images using Jetraw** within LabView.  
<br/>For more info visit:
https://www.jetraw.com/

## Requirements
- **Jetraw installed** on a Windows computer (MacOS and Linux coming soon) and installation folder must be in PATH environment variable.<br/>
*Note:* if you do not have Jetraw installed visit https://www.jetraw.com/downloads/software and for usage information https://github.com/Jetraw/Jetraw
- **LabView 2020 installed** for Windows 64 bits.<br/>
*Note:* other versions can work as well but the installation package would need to be generated for the specific target. 
- For writing compressed files a **valid License** is needed and a calibration file for the camera.  


## Installation
You will need the following NIPKG file for installation:

- jetraw_21.07.01.1_windows_x64.nipkg [latest (pre-)release](https://github.com/Jetraw/LabView/releases/download/21.07.01.1/jetraw_21.07.01.1_windows_x64.nipkg)
  
If you need a previous version please go to [previous versions.](https://github.com/Jetraw/LabView/releases/

After the file is downloaded you simply need to double click on it and the installation process will start. Follow the installation steps. 

## Usage
Once the installation process is over you should be able to see the following VI blocks in your LabView:

- dpcore_init_and_prepare.vi:<br/>It initializes dpcore and the input image is prepared to be ready for compression. Remember to add the correct camera id for the calibration. At the moment there is a hard-coded value by default. 
- jetraw_compress.vi:<br/>It compresses the input buffer (already dpcore prepared, if not it will fail). 
- jetraw_decompress.vi:<br/>It decompressed the input buffer. 
- jetraw_tiff_compress_and_save.vi:<br/>It compressed the input buffer (already dpcore prepared) and saves the compressed image in a TIFF file. Right now the saving path is relative to the module, therefore some modifications might be needed by the user. 

You can also follow the examples that you will find in this repository:
- compress_tiff_buffer_example.vi
- compress_tiff_example.vi

## Contact
Feel free to use the [issues section](https://github.com/Jetraw/LabView/issues) to report bugs or request new features. You can also ask questions and give comments by visiting the [discussions](https://github.com/Jetraw/LabView/discussions), or following the contact information at https://jetraw.com.