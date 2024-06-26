# Morning Glory Detection
[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](LICENSE)

A detection tool with Matlab UI.

📃 [Read the Full Paper](https://www.mdpi.com/2624-7402/6/1/34).

## Instruction:
Need to install Matlab first.\
Run "main.m" to activate the app interface.  

Play with the following steps:
1. Click "Open New Image" to load the image you want to detect. Browse and choose the image in the pop-up window.\
   <img src="Figs/img1.png" alt="Sample Image" width="600"/>
2. Choose the segmentation method for shadow removal, and click "Segment" to apply it.
	- 2.1 K-means
		The parameter of K-means is the number of the cluster. The default k equals 3. Small k's can avoid most of the noise in the shadow. Larger k provides more details.
	- 2.2 Mean shift
		The parameter of Mean shift is the bandwidth of the kernel. The default bw equals to 0.2. It's a faster method for segmentation. The detection result is very similar to the K-means when k = 3.
    <img src="Figs/img2.png" alt="Sample Image" width="600"/>
3. Click "Mask" to generate the binary mask for shadow removal.\
   <img src="Figs/img3.png" alt="Sample Image" width="600"/>
4. Click "Output" to get the detection result.\
   <img src="Figs/img4.png" alt="Sample Image" width="600"/>
5. (optional) Save the image.
6. Click "Count" to count the number of detected clusters.\
   <img src="Figs/img5.png" alt="Sample Image" width="600"/>

* After each step you might need to wait for a few seconds to see the image change, which indicates the current step finished. 
  The waiting time depends on the input file size and computing speed.

* This app referenced the mean shift method from *K. Fukunaga and L.D. Hosteler, 
  "The Estimation of the Gradient of a Density Function, with Applications in Pattern Recognition".* [PDF](https://ieeexplore.ieee.org/document/1055330)

## Citation

@article{valicharla2024morning,
  title={Morning Glory Flower Detection in Aerial Images Using Semi-Supervised Segmentation with Gaussian Mixture Models},
  author={Valicharla, Sruthi Keerthi and Wang, Jinge and Li, Xin and Gururajan, Srikanth and Karimzadeh, Roghaiyeh and Park, Yong-Lak},
  journal={AgriEngineering},
  volume={6},
  number={1},
  pages={555--573},
  year={2024},
  publisher={MDPI}
}
