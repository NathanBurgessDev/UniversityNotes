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

- Does it terminate for all values of $n \ge 1$?

- for $n=7$
```
7, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1
```

- It is impossible to write a program that decides if another program terminates

### Proof 
- Imagine a program that can determine if a program can terminate or not 
- Add to the end of it 
	- if the program halts -> loop 
	- if the program loops -> halt
- feed the program into itself 
