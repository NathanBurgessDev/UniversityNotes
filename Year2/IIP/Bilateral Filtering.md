
### Bilateral Filtering 

- Anistropic Diffusion is related to mean filtering 
- If the similarity function is always 1 we get a mean filter 
![[Pasted image 20230223135148.png]]

- Bilateral filters modify Gaussian smoothing in a similar way 
	- One Gaussian weights pixels that are near the source 
	- Another Gaussian weights pixels that have similar intensity to the source pixel 

