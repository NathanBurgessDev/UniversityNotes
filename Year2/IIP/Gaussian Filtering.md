
### Gaussian Filters 

- Convolution with a mask whose weighst are determined by a 2D Gaussian function 
- Higher weight is given to pixels near the source pixel 
- These are more likely to lie on the same object as the source pixel 
![[Pasted image 20230214151516.png]]


### Discrete Gaussian Filters 

- The Gaussian
	- extends infinitely in all directions but we want to process just a local window 
	- has a volume underneath it of 1 which we want to maintain 
- We can approximate the Gaussian with a discrete filter 
	- we restrict ourselves to a square window and sample the Gaussian function 
	- We normalise the result so that the filter entries sum to 1 
![[Pasted image 20230214151756.png]]

