# Reflections June 19

## Web Dev

### Regular Expression

Today i've learned topics about regular expression

Using the test method to see if we found the regex in the string
In the example below we are matching it with literal strings but what about
other possibilities?

```
Example
    let str = "Hello, World";
    let regex = /Hello/;
    let result = regex.test(str);
    this will return true
```

I also learned about extracting matches instead
```
    I will reuse the example above
    let result = str.match(regex);
    will return the matched pattern which is Hello
```

Matching literal string with different possiblities
using the | or operator
```
    let petString = "James has a pet cat.";
    let petRegex = /dog|cat|bird|fish/; 
    let result = petRegex.test(petString);
```

Ignore Case while Matching and Find more than first match
- I can do this by using flags 

```
    /l/g - global flag which find more than the first match
    if we match this we will get two l
    /hello/i - ignore case flag find whether its upper or lower
    we will get Hello because it ignores  
```

Match anything with a Wildcard and Single char with multiple possiblities

Wildcard period
```
let humStr = "I'll hum a song";
let hugStr = "Bear hug";
let huRegex = /hu./;
humStr.match(huRegex); // Returns ["hum"]
hugStr.match(huRegex); // Returns ["hug"]
```

Single char multiple possibilities using a charset
```
let bigStr = "big";
let bagStr = "bag";
let bugStr = "bug";
let bogStr = "bog";
let bgRegex = /b[aiu]g/;
bigStr.match(bgRegex); // Returns ["big"]
bagStr.match(bgRegex); // Returns ["bag"]
bugStr.match(bgRegex); // Returns ["bug"]
bogStr.match(bgRegex); // Returns null
```

Using Charset
it might be tedious to do
[abcdefg]
there is sa better solution which is using a hyphen to indicate a range
```
Example
    [a-z]
    [0-9]
    [a-zA-Z0-9] // indicates that characters lowercase a to z and uppercase A-Z 0-9
```

Negated Charset
- We can also create characters we dont want to match using negated character set
- To create one we use the caret symbol ^ after the opening bracket

```
Example
    /[^aeiou]/gi matches all characters that are not a vowel
```

Matching characters that occur One or more times/ Zero or more times
the + character allow us to match something that repeat consecutively
```
    For example, 
    /a+/g would find one match in "abc" and return ["a"]. 
    Because of the +, it would also find a single match in "aabc" and return ["aa"].
```

the * star allow us to match char that occurs zero or more times
```
    For Example,
    let soccerWord = "gooooooooal!";
    let gPhrase = "gut feeling";
    let oPhrase = "over the moon";
    let goRegex = /go*/;
    soccerWord.match(goRegex); // Returns ["goooooooo"] it see that o occurs multiple times
    gPhrase.match(goRegex); // Returns ["g"] it see that g exist but o doesnt so it only returns g
    oPhrase.match(goRegex); // Returns null it see that g and o doesn't exist so it says null
```


