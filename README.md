TIGRE: Tomographic Iterative GPU-based Reconstruction Toolbox
======

IGRE is an open-source toolbox for fast and accurate 3D tomographic 
reconstruction for any geometry.  Its focus is on iterative algorithms 
for improved image quality that have all been optimized to run on GPUs 
(including multi-GPUs) for improved speed.  It combines the higher level 
abstraction of MATLAB or Python (in two separate branches of the 
toolbox) with the performance of CUDA at a lower level in order to make 
it both fast and easy to use.

TIGRE is free to download and distribute: use it, modify it, add to it, 
share it.  Our aim is to provide a wide range of easy-to-use algorithms 
for the tomographic community "off the shelf".  We would like to build a 
stronger bridge between algorithm developers and imaging 
researchers/clinicians by encouraging and supporting contributions from 
both sides into TIGRE.

TIGRE remains under development as we are still adding new features 
(e.g., motion compensation).  If you have any request for a specific 
application, do not hesitate to [contact us](mailto:ander.biguri@gmail)!

 - [TIGRE features](#features)
 
 - [Installation instructions](#installation)
 
 - [FAQ](#faq)
  
 - [Further reading](#further-reading)
 
 - [Contact](#contact) 
 
 - [License](#licensing)



## Features

TIGRE is, mainly, a GPU-based CT recosnturction tool that contains a wide range of iterative algorithms.

TIGRE features:

- A MATLAB and python library for high performance multi-GPU based X-ray absorbtion tomography recosntruction

- State of the art implementations of projection and backprojection operations on GPUs, with easy interface with higher level languages in order to ease delevoping of new methods.

- **Flexible CT geometry:** Cone Beam, Parallel Beam, Digital Tomosynthesis, C-arm CT, an any other geometry. Geometric parameters are defined per projection, not per scan.

- A wide range of recosntruction algorithms for CT

	- Filtered Backprojection (FBP,FDK) and variations (different filters, Parker weights, ...)
	
	- **Iterative algorithms** 
	    
		- Gradient based algorithms (SART, OS-SART, SIRT) with multiple tuning parameters (Nesterov acceleration, initialization, parameter reduction, ...)
		
		- Krylov Subspace algorithms (CGLS)
		
		- Statistical recosntruction (MLEM)
		
		- Total Variation regularization based algorithms: FISTA-based (SART-TV) and POCS based (ASD-POCS, OS-ASD-POCS, B-ASD-POCS-β, PCSD, AwPCSD, Aw-ASD-POCS)
		
- TV denoising for 3D images
		
- Basic image loading fucntionality
		
- A variety of plotting functions
		
- Image quality metrics.
	

## Installation

Both MATLAB and Python builds are fully supported.

- [Installation instructions and requirements for MATLAB](Frontispiece/MATLAB_installation.md).

- [Installation instructions and requirements for Python](Frontispiece/python_installation.md).

## FAQ

For answers to frequently asked questions [click here](Frontispiece/FAQ.md).

## Gallery

To see a gallery of images on different CT modalities recosntructed using TIGRE [click here](Frontispiece/Gallery.md)

<img src="https://raw.githubusercontent.com/AnderBiguri/PhDThesis/master/Applications/randofull.png" height="400">



## Further Reading

If you want more formal/academic information on TIGRE and its algorithms, [click here](Frontispiece/Further_reading.md).

## Contact

Contact the authors directly at

[tigre.toolbox@gmail.com](mailto:tigre.toolbox@gmail.com) or [ander.biguri@gmail.com](mailto:ander.biguri@gmail.com)

## Licensing

TIGRE has been created jointly by the University of Bath's 
Engineering Tomography Lab and CERN

The TIGRE toolbox is released under the BSD License, meaning you can use and modify 
the software freely. However, you **must** cite the original authors.
For more information read [the licence file][1] or the [BSD License Definition][2].

If you use TIGRE, please reference the following paper:

**TIGRE: A MATLAB-GPU toolbox for CBCT image reconstruction**
*Ander Biguri, Manjit Dosanjh, Steven Hancock, and Manuchehr Soleimani*
**Biomedical Physics & Engineering Express, Volume 2, Number 5**
[Read the article (Open Access)][3]

[1]: LICENSE.txt
[2]: http://www.linfo.org/bsdlicense.html
[3]: http://iopscience.iop.org/article/10.1088/2057-1976/2/5/055010
