## Language Table
| Type   | Language Type                                           | Automata          |                         |
| ------ | ------------------------------------------------------- | ----------------- | ----------------------- |
| Type 3 | Regular langauges                                       | Finiate automata  | Regular expression      |
| Type 2 | Context free languagees                                 | Pushdown automata | Context free expression |
| Type 1 | Context sensitive                                       | Turing machines   | Grammar $\lambda$       |
| Type 0 | Recursively enumerable languages -> Decidable languages |                   |                         |




## The Halting Problem

``` C
while (n > 1) {  
	if even(n) {  
		n = n / 2;  
	} else {  
	n = n * 3 + 1;  
	}  
}
```

- Does it terminate for all values of $n \ge 1$
- 