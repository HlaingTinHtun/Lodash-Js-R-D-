# Filter

- Filtering a list to transform the elements we want to get back

```
var numbers = _.range(0,10);      // [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

var evenNumbers = _.filter(numbers, function(e){ return e % 2 != 0; });
// evenNumbers is now [ 0, 2, 4, 6, 8 ]
```

# Reduce

- Reducing a list of objects to a single value. 
- Ex=>A group of people can buy a meal or not. In that case we have to check out they have the enough amount by the sum of money they have.
- (Each's money => sum money)

```
var ppl = [
    {
        'name': 'Keita',
        'money': 1000
    },
    {
        'name': 'Sato',
        'money': 3000
    },
    {
        'name': 'Ruma',
        'money': 500
    },
]

var sumMoney = function(data){
    return _.reduce(
        data,
        function(accumulated, e){
            return accumulated + e.money;
        },
        0
    );
}

function canBuyMeal(data){
    return 3500 < sumMoney(data);
}

canBuyMeal(ppl);    // returns true
```

# Some

- If there is at least one record in a collection that meets some criteria.

```
var ppl = [
    {
        'name': 'Keita',
        'hasMoney': true
    },
    {
        'name': 'Sato',
        'hasMoney': false
    },
    {
        'name': 'Ruma',
        'hasProperty': true
    },
]

function canLive(data){
    return _.some(data, function(e){ return e.hasProperty; });
}

canGroupDrive(ppl);    // returns true
```

# Map

- Useful for changing a list into a different list in a purely declarative way.
- Can just specify how you want to manipulate an element of a list.
- Make a new list transformed by providing a function

```
var res1 = _.range(5);       // [ 0, 1, 2, 3, 4]

var res2 = _.map(a, function(e){ return e + e;} );

result is [0, 2, 4, 6, 8]
```


