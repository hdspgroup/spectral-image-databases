# Hyperspectral and Multispectral images acquired in the HDSP optics Laboratory

## Databases acquired with the color coded aperture snapshot spectral imager (C-CASSI) architecture

The C-CASSI was assembled in the High Dimensional Signal Processing Group optics laboratory, at the Universidad Industrial de Santander in Bucaramanga, Colombia. More information about the databases and the experimental setup can be found in the paper [1].

[1] N. Diaz, H. Rueda, H. Arguello, "Adaptive filter design via a gradient thresholding algorithm for compressive spectral imaging", Appl. Opt. 57 (17) (2018) 4890–4900. doi:10.1364/AO.57.004890. URL http://ao.osa.org/abstract.cfm?URI=ao-57-17-4890


### Experimental Setup

The C-CASSI was assembled, in accordance with \cite{Rueda:15}, using a DMD-based implementation of colored coded apertures. The optical scheme depicts two arms, the imaging arm and the integration arm. In the imaging arm; the imaging lens focuses the light into the DMD.  Due to the DMD rotation angle of <img src="https://latex.codecogs.com/png.latex?$45^\circ$" title="$45^\circ$" /> relative to the detector pixels, the alignment of the optical elements is critical.  In order to correct for the inclination of the DMD, the elements in the integration arm of the setup are rotated <img src="https://latex.codecogs.com/png.latex?$45^\circ$" title="$45^\circ$" />, including the relay lens, the filter wheel, the prism, and the FPA. The apparatus is made up of:

1. An AC254-100-A-ML objective lens (Thorlabs)
2. A DLI4130 DMD (DLInnovations) with spatial resolution of <img src="https://latex.codecogs.com/png.latex?$1024&space;\times&space;768$" title="$1024 \times 768$" /> and mirror pitch size of <img src="https://latex.codecogs.com/png.latex?13.68&space;\mu&space;m" title="13.68 \mu m" />
3. A MAP10100100-A relay lens (Thorlabs)
4. An Amici Prism (Shanghai Optics)
5. A monochrome charged-coupled device detector (AVT Stingray F-145B) with spatial resolution <img src="https://latex.codecogs.com/png.latex?$1388&space;\times&space;1038$" title="$1388 \times 1038$" /> and pitch size of <img src="https://latex.codecogs.com/png.latex?6.45&space;\mu&space;m" title="6.45 \mu m" />.

The emulation of the CCA using the DMD and the set of optical filters is as follows: each CCA is mapped to a 3D array of block-unblock coded apertures paired with the corresponding set of optical filters, as described in \cite{Rueda:15}, thus emulating the colored coded aperture. Each pair of filter and block-unblock coded aperture is calibrated to characterize the impulse response of the system, which uses as input a monochromatic light, and a white plate as the target. The compressive measurements are obtained using as a target the real scene instead of the white plate and replacing the monochromatic light with a broadband white light. If each band is set to be encoded independently, a single shot acquisition with L bands will require L switches in the DMD, and L rotations of the filter wheel. Experimentally, the DMD switching time is <img src="https://latex.codecogs.com/gif.latex?\sim&space;50&space;\mu&space;s" title="\sim 50 \mu s" /> and the rotation time of the filter wheel is <img src="https://latex.codecogs.com/gif.latex?$\sim&space;50&space;ms$" title="$\sim 50 ms$" />, being the latter the bottleneck. Therefore, the largest integration time for a single shot is bounded by <img src="https://latex.codecogs.com/gif.latex?$50&space;L&space;ms$" title="$50 L ms$" />.

[2] H. Rueda, H. Arguello, and G. R. Arce, "DMD-based implementation of patterned optical filter arrays for compressive spectral imaging", J. Opt. Soc. Am. A 32, 80–89 (2015).

### Real Multispectral Scenes
Two target scenes were used to evaluate the quality of image reconstruction of the adaptive C-CASSI against non-adaptive C-CASSI. Figure \ref{12} depicts the two targets. In this setup, the 3D block-unblock representation of CCA is loaded in the DMD, and each 2D slice is paired with the corresponding color filter placed in the filter wheel. Afterwards, the measurements is obtained by adding the 2D measurements. The experimental setup is synchronized, such that the DMD sets the pattern and the sensor captures the projection. After that, the DMD updates the coded aperture, and the filter wheel rotates. Subsequently, the detector measures the next projection. The first target is the bear-stars scene (left), and the second target is the flower-stars scene (right). The spatial resolution of the target scenes is $128 \times 128$. In the characterization of the Amici prism, $L=11$ spectral bands are resolved. The corresponding wavelength intervals are: $\{423 - 436\}$; $\{437 - 448\}$; $\{449-463\}$; $\{464-479\}$; $\{480-499\}$; $\{500-521\}$; $\{522-546\}$; $\{547-577\}$; $\{578-618\}$; $\{619-673\}$; $\{674-700\}$  nanometers.
