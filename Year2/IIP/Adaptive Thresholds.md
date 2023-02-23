
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