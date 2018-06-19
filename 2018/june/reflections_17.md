# Reflections June 17

## Web Development

Today i've learned plenty of stuff from advance functions and advance array topics

### Advance Functions
- Closure
    All Functions are closure having access outside of its scope and having the ability for functions to have private variables
- Currying 
    Currying is adding prefixed values or providing arguments one by one not on one line 
    ```
    Example: 
    var greet = (greeting) => (name) => `${greeting} ${name}`;
    greetHello = greet("hello");
    (name) => `${greeting} ${name}`
    greetHello("Vincent");
    "hello Vincent"
    ```
- Composing
    Composing is applying multiple functions at once.

### Advance Arrays
- map
    Mapping is similar to a foreach but i think it's a much better way to iterate through an array
    because it creates a new array for you and you need to return a value which will copy it to the array
    that is being created. And it follows the deterministic principle
    ```
    Example:
    const arr = [1, 2, 3, 5 , 7, 4];
    const mapArr = arr.map(num => {
        return num * num;
    });
    We are mapping each array to another array
    and the result would be
    mapArr = [1, 4, 9, 25, 49, 16];
    ```
- filter
    Filter is a way to return values with conditions. To filter things as it names states
    ```
        Example:
        const arr = [1,2,3,4,5,6,7,8,9,10];
        const filterArr = arr.filter (num => num > 5);

    Result: filterArr = [6,7,8,9,10];
    ```
- reduce
    reduce aims to apply a function agaisnt an accumulator to reduce an array into a single value
    ```
    syntax:
        const array = [1,10,5];
        const reduce = array.reduce((accumulator, value) => {accumulator + value;}, 0);
        the zero up there is the initial value of accumulator you could also leave it blank
        and it will be zero or you could specify the value of accumulator.
    ```
    With the function above we have three values which 1, 10, 5  with reduce we are aiming to make it 
    a single value and to do so we are adding each number. before without reduce
    what we have to do is
    ```
        const newArr = []
        for (let i = 0, sum = 0; i < array.length; i++) {
            sum += array[i];
            newArr.push(sum);
        }
    ```
    which is more tedious without the reduce method