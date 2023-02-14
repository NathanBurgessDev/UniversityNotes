
## Spatial Filtering 
![[Pasted image 20230214140149.png]]

- Intensity Transforms read and affect only a single pixel
	- their power is limited 
- Images are spatially organised data structures many important attributes vary slowly across the image 
	- Object identity 
	- Viewed surface orientation, colour, etc
	- Illumination
- Processes restricted to a small compact area have access to more information but are still likely to consider a signle object surface illumination pattern etc

### Image Noise

- = small errors in image values
- imperfect sensors intorudce noise
- image comporession methods are lossy
	- added from repeated coding and decoding 
![[Pasted image 20230214140409.png]]

### Gaussian Noise 
- Sensors often give a measurement a little off the true value
	- on average they give the right value
- We model this with a **gaussian**
- Mean (μ) = 0
- Variance (σ$^2$ ) indicates how much noise there is
![[Pasted image 20230214144848.png]]


- The level of noise is related to the **Gaussian parameter ** $\sigma$
![[Pasted image 20230214144947.png]]

### Noise Reduction 

- If you have multiple images
	- taking the mean value of each pixel will reduce noise
	- noise is randomly added to each value
	- mean value added = 0
	- if you average a a large set of estiamtes of the same pixel the random noise values will cancel out 
- e.g 
	- 42 43 44 41 40 42 42 44 40
	- -> 42 

- Given only a single image averaging over a local region has a similar effect
![[Pasted image 20230214145416.png]]

- Ideally we would choose the region to only include pixels that should have the same value 
- Solution 
	- Spatial filter 

### Spatial Filtering: Convolution 

- Many filters follow a similar pattern
	- multiplying each image value by a corresponding filter entry and summing the results 
![[Pasted image 20230214145530.png]]

### Filtering 

- More generally with a filter of radius r
![[Pasted image 20230214145710.png]]

- Many, though not all filters work this way 
![[Pasted image 20230214145726.png]]

### The mean filter
![[Pasted image 20230214145745.png]]

