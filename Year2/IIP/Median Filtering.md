
### Salt and Pepper noise 

- Sometimes sensors fail to respond or saturate in errror
	- false saturation gives a white spot in the image (salt)
	- failed response gives a black spot in the image (pepper)
	- Speckle Noise 
![[Pasted image 20230223131456.png]]

### Reducing Salt and Pepper Noise 
![[Pasted image 20230223131521.png]]

### The Median Filter 

- The median filter is an alternative 
	- The median is the middle value in a set 
	- Each pixel is set to the median value in a local window 
	- Result is a real pixel value not a combination 
	- 