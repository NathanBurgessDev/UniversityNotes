
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