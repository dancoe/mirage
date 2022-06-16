# Simulating JWST NIRCam images of a galaxy cluster with MIRAGE

MIRAGE simulated NIRCam images of the galaxy cluster MACS0647+70 and the triply-lensed z=11 candidate MACS0647-JD. This cluster simulation is meant to complement simulated blank field data from 
[JADES](https://fenrir.as.arizona.edu/jaguar/) and 
[CEERS](https://ceers.github.io/releases.html).
Plus I provide analysis tools for the NIRCam imaging.

JWST GO 1433 public data upcoming Nov 2022  
7 filters: F115W F150W F200W F277W F356W F444W F480M  
0.04" / pixel image reductions (native SW ~0.03", LW ~0.06")  
slight misalignments between short and long wavelength images  
4 dithers INTRAMODULEX cover short wavelength detector gaps  
F200W has 2 epochs (8 exposures)  

Galaxies modeled as Sersic profiles derived from CLASH HST F160W images  
NIRCam predicted fluxes from BAGPIPES SED fitting to CLASH HST 17-band photometry  

✔ [HST catalog & Sersic fits](https://github.com/dancoe/mirage/blob/master/MACS0647%20Galaxies%20HST%20Sersic%20fits.ipynb) – (Astropy.photutils, Astropy.modeling)  
✔ NIRCam predicted fluxes in each filter – (BAGPIPES)  
✔ [NIRCam simulated images](https://github.com/dancoe/mirage/blob/master/Simulate%20NIRCam%20Images%20MACS0647%20F277W.ipynb) – (MIRAGE)  
✔ [Processed & combined](https://github.com/dancoe/mirage/blob/master/Reduce%20NIRCam%20Simulated%20Images%20MACS0647%20F277W.ipynb) – (JWST Pipeline; CEERS tips & scripts)  
✔ [Color images](https://github.com/dancoe/mirage/blob/master/Trilogy%20color%20images%20NIRCam%20MACS0647.ipynb) – (Trilogy: updated for Python 3 notebook)  
✔ [NIRCam detections](https://github.com/dancoe/mirage/blob/master/MACS0647%20NIRCam%20detections.ipynb) – (Astropy.photutils)  
✔ NIRCam PSF-matched multiband photometry – (Astropy.photutils)  
✔ [Inspect NIRCam photometry](https://github.com/dancoe/mirage/blob/master/MACS0647%20NIRCam%20photometry%20results.ipynb)  

To do list:  
? Add lensed fainter & higher-z galaxies – (e.g., Aaron Yung SAMs)  
☐ Incorporate HST images to photometry + SED fitting  
☐ Galaxy detection & analysis – (Astropy.photutils, BAGPIPES)  
☐ Distinguish stars (brown dwarfs) from galaxies (as in LePhare)  

Inputs:
* [CLASH](https://archive.stsci.edu/prepds/clash/) [HST images of MACS0647](https://archive.stsci.edu/missions/hlsp/clash/macs0647/data/hst/scale_65mas/)
* [cleaned segmentation map of detections](https://github.com/dancoe/mirage/blob/master/z11_seg_cleaned.fits.gz)
* APT outputs: [XML](https://github.com/dancoe/mirage/blob/master/JWSTz11_NIRCam.xml), [pointing](https://github.com/dancoe/mirage/blob/master/JWSTz11_NIRCam.pointing)

Output image pixel size choice 0.04":
- Similar to strategy adopted for HST 0.06" reductions (native ACS 0.05", WFC3/IR 0.13")
- With 4 dithers, can almost improve resolution 2x with some artifacts; 0.06" -> 0.04" is smooth
- Higher resolution 0.02" pixel images may also be desirable especially for SW images

https://stsci.box.com/v/coe-nircam-mirage

https://github.com/dancoe/mirage

https://dancoe.space/jwst/simulations

![color image](MACS0647_color.jpg)