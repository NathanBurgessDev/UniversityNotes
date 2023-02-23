
### Otsu Thresholding 

- Assumes histograms are bimodal: two regions can be separated by one threshold 
- Think of the histogram as made of two normal (Gaussian) distibutions, described by their means and deviations 
- If a threshold is wrong it will include histogram bins from peak A in peak B
	- Peak A's deviation will be too small
	- Peak B's deviations will be too big 
	- Peak A's size (area) will be too small
	- Peak B's size will be too big 
![[Pasted image 20230223140922.png]]

- Find the threshold which minimises a wieghted sum of the variations of the two regions that threshold produce
- Weights are the areas of the histogram assigned to each region

- Find the threshold which minimises a weighted sum of the variations of the two regions that threshold produce
- Weights are the areas of the histogram assigned to each region 
![[Pasted image 20230223141601.png]]
- This is small when the two regions are both physically small and have low deviations 

### The Algorithm

- Consider all possible threshold (0-255)
- compute weighted sum
- pick *t* with smallest value 
- A recursive versions exists that is very efficient 

![[Pasted image 20230223141713.png]]

### Unimodal Thresholding 

- Many histograms are not bimodalthere is often ony one peak e.g. text is mainly white with a small amount of black
- Rosins unimodal methods
	- finds the peak
	- draws a line from there to teh top of the furthist bin
	- fidns the top of the bin that is furthist from this line; that bin value is the threshold 

