
## Sampling 
- Digitisation of the *spatial coordinates*
- Determines *spatial resolution*

### Nyquist Rate 
- Samples mustb e taken at a rate which is
	- twice the frequency of the highest frequency component to be reconstructed
- Under sampling 
	- sampling at a rate that is too coarse
	- i.e. below the Nyquist rate 
- Aliasing
	- artefacts that result from under sampling 

### Aliasing 
- Occurs when two signals become indistinguishable when sampled
- In our case the two signals are the true image (the image that would be seen if there were no quantisation) and the one reconstructed by the human vision system from a sampled image 

### Anti-aliasing 
- Aliasing can be introduced when an image is resampled, if the sampling rate of the new image is less than the Nyqust rate of the original 
- Smooth out high frequency signals before sampling so its imossible to see the alias 

## Quantisation
- Digitisation of the *light intensity function*
- Determines *grey level, colour or radiometic resolution*

- How many grey levels to store
- Determines the umber of levels of color  intesity to be represented at each pixel
- Sampling and quantisation occur naturally during image acquisition but can also be applied to existing images 

## Re-Sampling 

- Most basic form of image processing 
![[Pasted image 20230209140349.png]]
- **Downsampling** - need to compute a summary pixel value from each local area 
	- mean / weighted mean etc

![[Pasted image 20230209140432.png]]
- **Upsampling** - need to interpolate from the known values to produce an estimate at the unknown pixels 
	- Average the known values in a local region centred on each unknown pixel, fit some kind of function through known values 

## Re-quantisation 
- Pixel valuesa re integers in a fixed range 
- Grey level resolution can be dropped by dividing each pixel value by a constant 
	- there is a side effect
	- cant increase grey level resolution of a single pixel
- **Super-resolution methods** exist that combine multiple exposures of the same scene so have more than one measurement of each pixel 