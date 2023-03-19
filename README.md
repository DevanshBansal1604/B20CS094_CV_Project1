# Image Matching and Image Stitching (Computer Vision Course Project-1)

This project is about Image Matching, using various available methods,  their results, and comparing-and-contrasting between them. This project also focuses on Image Stitching, which is a practical use case scenario of Image Matching. This project can stitch any number of images and generate a panorama of them. This project also highlights my modification to traditional Harris Corner Detection Algorithm, and the results prove that my modification can be applied as an add-on after the traditional Harris Corner Detection for better performance.

## How and What to Install

If you are intending to use the .ipynb file, then nothing is required for installation.
If you are intending to use the .py file, then make sure following libraries/dependencies are installed in your system:

- python
- numpy
- cv2

## Usage of .ipynb File

- Downlaod the zip of the project and extract all of the files and folders available
- Open the .ipynb file in supporting platform like Google Colab or Jupyter Notebook
- Run all the cells
- You will be asked to provide 'number of images to be stitched' and their paths, for image stitching. No other cell requires user input.
- You can change images used in 'Image Matching' section, 'NMS v/s non-NMS' section; but don't forget to fine-tune the thresholds and kernel-size.

## Usage of .py File

- Downlaod the zip of the project and extract all of the files and folders available
- Run the python file in a terminal/powershell (if Windows OS) using following code:
```
$ python filename.py
```
- First Input will be asked from the user regarding Image Stitching, as no other thing requires user input, so enter the number of images to be stitched (as asked)
- Then enter the path of images to be stitched, considering the Note printed in the output

## Images

Some of the results are shown here:

Key-Point Matches of Harris Corners as Key-Points:

![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/Harris_Corner_Matches.png](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/Harris_Corner_Matches.png)

Key-Point Matches of SIFT Key-Points:

![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/SIFT_Matches.png](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/SIFT_Matches.png)

Images to be stitched:

![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Data/3a.jpeg](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Data/3a.jpeg)
![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Data/3b.jpeg](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Data/3b.jpeg)
![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Data/3c.jpeg](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Data/3c.jpeg)

Stitched Image using SIFT:

![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/SIFT_LR_123_3.png](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/SIFT_LR_123_3.png)

Harris-Corners without NMS:

![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/HC.png](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/HC.png)

Harris-Corners with NMS:

![https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/HC_NMS.png](https://github.com/DevanshBansal1604/B20CS094_CV_Project1/blob/master/Results/HC_NMS.png)

## Notations used in Naming of files in Data Folder

(Note: | is concatenation, and (a/b/c) denotes any one of the available choices)

- `homography` is used for Image Matching
- `box` is used for Harris Corner with NMS v/s Harris Corner without NMS
- `number|(a/b/c)` is the format of images used for Image Stitching, where the number denotes which images are to be stitched together, and left-to-right order of images is being given by alphabets at the end of the name

## Notations used in Naming of files in Results Folder

(Note: | is concatenation, and (a/b/c) denotes any one of the available choices)

- `Harris_Corner_Matches` is result file of Image Matching with Harris Corners as Key-Points
- `SIFT_Matches` is result file of Image Matching with SIFT Key-Points
- `algorithm_(LR/RL)_(12/123/23)_(1/2/3/4)` is the format of stitched images, where the algorithm is the method of Key-Point Detection, LR/RL denotes the method used to stitch the image, i.e. left-to-right or right-to-left respectively, 12/23/123 denotes the images stitched to form the resulting image and finally 1/2/3/4 denotes which of the set of images was stitched
- `HC` is result file of Harris Corners without NMS
- `HC_NMS` is result file of Harris Corners with NMS









