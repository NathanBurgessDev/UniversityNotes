
### Intesity Transforms Diagram

![[Pasted image 20230209151910.png]]

### Linear Transforms
- Multiplication by and addition of a constant 
- $g(x,y) = a.f(x,y) + b$
- Where:
	- a - the *gain*, controls contrast
	- b - the *bias*, controls brightness

### Gain
![[Pasted image 20230209152154.png]]

### Bias 
![[Pasted image 20230209152210.png]]

### Negation 
![[Pasted image 20230209152244.png]]

- Often used to make fine details more visable 

![[Pasted image 20230209155334.png]]

### Dynamic Range 
- Digital images are sampled 
	- contain a fixed number of data values
- Digital image representations can only store a fixed number of values
- Itensity transforms can produce values that are
	- outside that range so cant be stroed
	- clustered in a small part of that range and so are hard to distinguish
- Some intensity transforms need data in a particular range 

### Contrast Stretching 
- To convert a source image in which intensities range from min to max to one in which they range from min to max 
![[Pasted image 20230209155553.png]]

### Non-linear Transforms 
- Thresholding 
![[Pasted image 20230209155644.png]]

### Grey Level Slicing 

![[Pasted image 20230209160223.png]]
![[Pasted image 20230209160232.png]]

### Gamma Correction 

- When an image is displayed on a screen the hardware used effectively applies an intensity transform 
- You send a voltage proportional to the intesnity of a pixel, the screen displays an intensity that is related to that but now how you may think
![[Pasted image 20230209160335.png]]
- We need to transform the image so that it generates a coltage which will display what we want
- create a new imagine in which 
![[Pasted image 20230209160410.png]]
- Gamma Correction because the equation is usually written
- $g(x,y) = f(x,y)^Y$

- 