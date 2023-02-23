
### Anisotropic Diffusion 

- Median filtering is good given small regions of speckle noise
	- less good if edges are important
- There are edge preserving operations 

- **Diffusion**
	- spreading out
	- mean and gaussian filters can be seen as diffusion processes
- **Anisotripic**
	- not the same in all directions 
- **The Basic idea**
	- Mean and Gaussian filters make each pixel more like its neighbours 
	- Anistropic diffusion makes each pixel more like those neighbours that it is already similar to

- We have a similiarity functions s(p,q)
	- s(p,q) has values in the range from 0 to 1 
	- If the pixels p and q are siilar than s(p,q) is close to 1
	- if the pixels p and q are different then s(p,q) is close to 0
- We use s(p,q) to compute a weighted average of pixel values 
	- the new value at a pixel, p , is based on all its neighbours, q

### The Similarity Function 

- The smoothing function, s(p,q)  needs to be fond 
- if *d* is the difference between *p* and *q*