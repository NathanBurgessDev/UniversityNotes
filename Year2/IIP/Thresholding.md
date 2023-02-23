### Binary Images 

- Many image processing operations make a decision
	- Is this what im interested in?
- The result is a binar image 
	- pixels can have only 2 values 0 or 1 
	- Binary images need noise removal enhancement etc

### Binarisation 

- A dark object on a light background in a grey-level image 
- Choose a threshold value, $T$
- Consider each pixel in turn
	- If the brightness at a pixel is less than T, that pixel is object 
	- Otherwise it is part of the background 
- Basic idea extends to colour, define sets of colour values that correspond to objects 

![[Pasted image 20230223140510.png]]

- The value of the threshold is very important
	- if it is too high background pixels will be classified as foreground 
	- if it is too low object pixels will be considered background 
- Assues there are exactly two regions with now overlap in their brightness *is that true?*

### Adaptive Thresholds 

- if the users choosees * t* for each of a set of images there is no guaranteee the results will be consistent
- Automatic methods choose a threshold based on image properties: histograms are commonly used

![[Pasted image 20230223140648.png]]