
$\Sigma = \{0,1\}$ Symbol before that is 1 

![[Pasted image 20230209111609.png]]

If there are multiple possible movements.
Use tokens to track all the possible tracks.

### Defitnition 
$NFA = \{Q,\Sigma, \sigma, S, F\}$

![[Pasted image 20230209112647.png]]

$Q = \{0,1,2,3,4,5\}$
$\Sigma = \{a,b,c\}$
$\sigma : Q × \Sigma \rightarrow P Q$
$Q \rightarrow \Sigma \rightarrow Q \rightarrow Prop$
$S \subseteq Q (S:Q \rightarrow Prop)$
$S = {0,4}$
$F \subseteq Q ( F : Q \rightarrow Prop)$
$F = \{1,2,3\}$

![[Pasted image 20230209113300.png]]

$\hat \sigma : Q \rightarrow \Sigma* \rightarrow Q \rightarrow Prop$

$\hat \sigma: q , xw , q' = \exists q'' : Q, \sigma q × q'' \land \hat \sigma q'' w q'$





