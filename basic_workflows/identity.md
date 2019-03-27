# Identity

```
var res = _.identity('hlaing', 'tin');
// res is hlaing
```
- Method returns the first argument

## _.identity in documentation of _.findKey and _.findLastKey

```
var data = {
    topic: "lodash",
    desc: "js library",
    awesome: "chaining"
};

var keyRes = _.findKey(p);        // returns "topic"
var lastKeyRes = _.findLastKey(p);    // returns "awesome"

// same with above 
var keyRes = _.findKey(p, _.identity);
var lastKeyRes = _.findLastKey(p, _.identity);

// which again means the same scenario:
var keyRes = _.findKey(p, function(x) { return x; }
var lastKeyRes = _.findLastKey(p, function(x) { return x; }
```
