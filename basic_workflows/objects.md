# has

- Determine if an object has (or contains) a key.

```
var obj = {
  data1: 2,
  data2: 3,
  data3: {
    data3_1:40,
    data3_2:{
      data3_2_1:500
    }
  }
};

var res1 = _.has(obj, "data1");          // true
var res2 = _.has(obj, "data1.data2");        // false
var res3 = _.has(obj, "data3");          // true
var res4 = _.has(obj, "data3.data3_2");       // true
var res5 = _.has(obj, "data3.res3_2_1");      // false
var res6 = _.has(obj, "data3.data3_1.data3_2_1");   // false
var res7 = _.has(obj, "data3.data3_2.data3_2_1");   // true
```

- Arrays can be used to split up parts.
```
var res8 = _.has(obj, ["data1", "data2"]);   // false, same as res2
var res9 = _.has(obj, ["data3", "data3_2"]);  // true, same as res4
```
