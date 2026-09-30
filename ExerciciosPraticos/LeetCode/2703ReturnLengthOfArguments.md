# 2703. Return Length of Arguments Passed
<p align="justify">
Write a function argumentsLength that returns the count of arguments passed to it.

```
Example 1:
Input: args = [5]
Output: 1
Explanation:
argumentsLength(5); // 1
One value was passed to the function so it should return 1.

Example 2:
Input: args = [{}, null, "3"]
Output: 3
Explanation: 
argumentsLength({}, null, "3"); // 3
Three values were passed to the function so it should return 3.
 
```
</p>    

## Solução
### Pensamentos e Anotações
<p align="justify">

</p>    

### Resultado
```
var argumentsLength = function(...args) {
    return args.length;
};

```