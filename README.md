# Hyperspectral and Multispectral images acquired in the HDSP optics Laboratory

## Databases acquired with the color coded aperture snapshot spectral imager (C-CASSI) architecture

The C-CASSI was assembled in the High Dimensional Signal Processing Group optics laboratory, at the Universidad Industrial de Santander in Bucaramanga, Colombia. More information about the databases and the experimental setup can be found in the paper [1].

>[1] N. Diaz, H. Rueda, H. Arguello, "Adaptive filter design via a gradient thresholding algorithm for compressive spectral imaging", Appl. Opt. 57 (17) (2018) 4890–4900. doi:10.1364/AO.57.004890. URL http://ao.osa.org/abstract.cfm?URI=ao-57-17-4890


### Experimental Setup

![Experimental Setup](https://github.com/hdspgroup/spectral-image-databases/blob/master/images/figure10.png)

The C-CASSI was assembled, in accordance with [2], using a DMD-based implementation of colored coded apertures. The optical scheme depicts two arms, the imaging arm and the integration arm. In the imaging arm; the imaging lens focuses the light into the DMD. Due to the DMD rotation angle of 45&#176; relative to the detector pixels, the alignment of the optical elements is critical.  In order to correct for the inclination of the DMD, the elements in the integration arm of the setup are rotated 45&#176;, including the relay lens, the filter wheel, the prism, and the FPA. The apparatus is made up of:

1. An AC254-100-A-ML objective lens (Thorlabs)
2. A DLI4130 DMD (DLInnovations) with spatial resolution of 1024 &#10005; 768 and mirror pitch size of 13.68 &#181;m
3. A MAP10100100-A relay lens (Thorlabs)
4. An Amici Prism (Shanghai Optics)
5. A monochrome charged-coupled device detector (AVT Stingray F-145B) with spatial resolution of 1388 &#10005; 1038 and pitch size of 6.45 &#181;m.

The emulation of the CCA using the DMD and the set of optical filters is as follows: each CCA is mapped to a 3D array of block-unblock coded apertures paired with the corresponding set of optical filters, as described in [2], thus emulating the colored coded aperture. Each pair of filter and block-unblock coded aperture is calibrated to characterize the impulse response of the system, which uses as input a monochromatic light, and a white plate as the target. The compressive measurements are obtained using as a target the real scene instead of the white plate and replacing the monochromatic light with a broadband white light. If each band is set to be encoded independently, a single shot acquisition with L bands will require L switches in the DMD, and L rotations of the filter wheel. Experimentally, the DMD switching time is &#8764; 50 &#181;s and the rotation time of the filter wheel is &#8764; 50 ms, being the latter the bottleneck. Therefore, the largest integration time for a single shot is bounded by 50 Lms.

>[2] H. Rueda, H. Arguello, and G. R. Arce, "DMD-based implementation of patterned optical filter arrays for compressive spectral imaging", J. Opt. Soc. Am. A 32, 80–89 (2015).


### Real Multispectral Scenes

![Experimental Setup](https://github.com/hdspgroup/spectral-image-databases/blob/master/images/figure11.png)

Two target scenes were used to evaluate the quality of image reconstruction of the adaptive C-CASSI against non-adaptive C-CASSI. The above figure depicts the two targets. In this setup, the 3D block-unblock representation of CCA is loaded in the DMD, and each 2D slice is paired with the corresponding color filter placed in the filter wheel. Afterwards, the measurements is obtained by adding the 2D measurements. The experimental setup is synchronized, such that the DMD sets the pattern and the sensor captures the projection. After that, the DMD updates the coded aperture, and the filter wheel rotates. Subsequently, the detector measures the next projection. The first target is the bear-stars scene (left), and the second target is the flower-stars scene (right). The spatial resolution of the target scenes is 128 &#10005; 128. In the characterization of the Amici prism, L=11 spectral bands are resolved. The corresponding wavelength intervals are: 423 - 436; 437 - 448; 449 - 463; 464 - 479; 480 - 499; 500 - 521; 522 - 546; 547 - 577; 578 - 618; 619 - 673; 674 - 700 nanometers.

This two real scenes can be downloaded from this repository in the following links:
* Bear-stars scene: 
* Flower-stars scene: 

### How to Cite
If you use any of the multispectral scenes showed above, or if the presented experimental assembly was useful for your research, please cite at least one of the following research works:

* ***Adaptive filter design via a gradient thresholding algorithm for compressive spectral imaging***
```
@article{diaz2018adaptive,
  title={Adaptive filter design via a gradient thresholding algorithm for compressive spectral imaging},
  author={Diaz, Nelson and Rueda, Hoover and Arguello, Henry},
  journal={Applied optics},
  volume={57},
  number={17},
  pages={4890--4900},
  year={2018},
  publisher={Optical Society of America}
}
```
* ***Adaptive grayscale compressive spectral imaging using optimal blue noise coding patterns***
```

```
