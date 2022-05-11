# Simulating JWST NIRCam images of a galaxy cluster with MIRAGE

MIRAGE simulated NIRCam images of the galaxy cluster MACS0647+70 and the triply-lensed z=11 candidate MACS0647-JD

JWST GO 1433 public data upcoming Nov 2022

7 filters: F115W F150W F200W F277W F356W F444W F480M  
0.04" / pixel  
slight misalignments between short and long wavelength images  
4 dithers INTRAMODULEX covers short wavelength detector gaps  
F200W has 2 epochs (8 exposures)  

CLASH HST F160W Sersic fits

NIRCam predicted fluxes from BAGPIPES SED fitting to CLASH HST 17-band photometry  

✔ HST catalog & Sersic fits – (Astropy.photutils, Astropy.modeling)  
✔ NIRCam predicted fluxes in each filter – (BAGPIPES)  
✔ NIRCam simulated image – (MIRAGE)  
✔ Processed & combined – (JWST Pipeline; CEERS tips & scripts)  
☐ Add lensed fainter & higher-z galaxies – (Aaron Yung SAMs)  
☐ Galaxy detection & analysis – (Astropy.photutils, BAGPIPES)  

https://stsci.box.com/v/coe-nircam-mirage

https://github.com/dancoe/mirage

https://dancoe.space/jwst/simulations

![color image](MACS0647_color.jpg)
