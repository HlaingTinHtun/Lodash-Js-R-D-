# Chaining
## Without Chaining
```
var data1 = [10, 15, 20, 25, 15];

var data2 = _.filter(data1, function(item){ return item % 10 === 5 });
// data2 now contains [15, 25, 15]

var data3 = _.uniq(data2);
// data3 now contains [15, 25]

var data4 = _.map(data3, function(item){ return item + 1 });
// data4 now contains [16, 26]
```

## With Chaining
```
var data1 = [10, 15, 20, 25, 15];

var data4 = _(data1)
    .filter(function(item){ return item % 10 === 5 })
    .uniq()
    .map(function(item){ return item + 1 })
    .value();
// data4 now contains [16, 26]
```
- The chaining is more efficient.
- no intermediate results are created.


# Slight Changes for `Explicit Chain` & `Implicit Chain`

## Explicit chaining 
### Still need to unwrap the result with .value().
    
 ```
 var data = [1, 5, 10, 15, 5, 10, 1, 20];

var unqSum = _.chain(data)
    .uniq()
    .sum()       
    .value();   
result is 51
 ```
## Implicit chaining 
### The "unwrapping" of the single value is implied. (there is no need to call .value().)
```
var data = [1, 5, 10, 15, 5, 10, 1, 20];

var unqSum = _(data)
    .uniq()
    .sum();  
    
    //result is 51
```  
    
 



