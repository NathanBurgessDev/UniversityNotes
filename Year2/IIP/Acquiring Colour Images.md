
- Each pixel in a grey level image contains one value
	- colour requires three
- RGB modle inspired by the retina is an obvious choice for cameras 
- Some cameras use complex optics and 3 CCDs to capture each colour channel independently 
- Necessary for some scientific purposes - not general use 

![[Pasted image 20230209140817.png]]

### Bayer Pattern 
- One colour value is measured but two are estimated at each pixel
![[Pasted image 20230209140910.png]]

### Representing Colour: RGB
- Most common starting point
- Retinal cells are sensitive to three primary colours T G B
- light not pigments 

![[Pasted image 20230209141029.png]]

### Colour vs Greyscale 

- Sometimes we want a single value at each pixel
	- processing is easier
	- reduces information
	- easier theory 
- Many image processing methods were developed for single value images 
- This value is usually intensity / grey level
- Early CCds only produced grey level; rare now 
	- we can compute the grey value using a siple average of red gree nand blue
	- however: our eyes are more sentive to green light 

### Converting from RGB to Greyscale 
- We can convert RGB to greyscale using 
- $i = 0.30r + 0.59g + 0.11b$

