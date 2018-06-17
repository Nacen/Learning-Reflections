# Reflections June 15

## Web Development

So today i've started learning more about javascript and topics about ES6

- let, const are new ways to declare a variable

- Destructuring
```

    const person = {
        firstname: "John",
        lastname: "Doe",
        age: 50,
        eyeColor = "blue"
    }
    before we had this
    const firstname = person.firstname;
    we can do this instead
    const {firstname} = person;
```
- default parameters and fat arrow
```
    function (age = 10) => age;
    fat arrow means this is a function and return what ever the arrow is pointing at
```

- template strings which is almost similar to string interpolation in c#

```
    Syntax:
    let message = `Hello I am ${firstname}`;
``` 

- and assigning variables to be an object property
```
    old way
    var a = 'test';

    var obj = {
        a = a;
    }

    new way
    var a = 'test';
    var newobj = {
        a;
    }
```

- Lastly Symbols 
```
    const symb = Symbol();
```