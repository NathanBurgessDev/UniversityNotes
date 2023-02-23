
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

- How big should the filter window be 
	- With Gaussian filters this depends on the variance 
	- Under a Gaussian curve 98% of the area lies within 2 $\sigma$ of the mean 
	- A filter width of 5$\sigma$ gives more than 98% of the values we want 
![[Pasted image 20230214152209.png]]

### Separable Filters 

- The Gaussian filter is separable
	- A 2D Gaussian is equivalent to two 1D Gaussians
	- first you filter with a horizontal Gaussian
	- Then a vertical Gaussian 
![[Pasted image 20230214152424.png]]
![[Pasted image 20230214152458.png]]

### Separable Filters 

- The separated filter is more efficient
	- Given an NxN image and a nxn filter we need to do O(N$^2$n$^2$)operations 
![[Pasted image 20230214153351.png]]

### More Gaussian SMoothing 