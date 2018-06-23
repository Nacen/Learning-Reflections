# Reflections June 20

## WebDev

### Regular Expressions 
- Lazy Matching
- Match Beginning String Patterns
- Match Ending String Patterns
- Match All Letters and Numbers 
- Match Everything But Letters and Numbers
- Match All Numbers 
- Match All Non-Numbers
- Match Whitespace 
- Match Non-Whitespace Characters
- Check for All or None
- Positive and Negative Lookahead
- Reuse Patterns Using Capture Groups

Lazy Matching

By default regular expressions are greedy.
What is greedy in regular expression?
- it aims to return the largest-substring possible to fit the pattern
While Lazy Matching is to return the smallest-substring possible 
- You can use the `?` character to change it to lazy matching.
```
Example is  "titanic" matched against the adjusted regex of /t[a-z]*?i/ returns ["ti"].
it returns ti because it matches t and the next character to ? will be the end of substring to be returned
```

Match Beginning String Patterns

You can use the caret character ^ to specify the beginning pattern
, woah didn't you use caret before?

yes we used caret on charset [^] to create a negated char set but now
we are using it to specify the beginning pattern, An example below
```
Example
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
// Returns true
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);
// Returns false
```

Match Ending String Patterns

Similar to begin string patterns, We use a dollar sign instead at the end of the pattern.
```
Example is 
let firstString = "Ricky is first and can be found.";
let firstRegex = /Ricky$/ // returns false
let secondString = "first is Ricky"; // returns true
```

Match All Letters and Numbers 

instead of doing [A-Za-z0-9] charset of A-Z a-z 0-9
You can do this by using \w, These shortcut character classes are also known as shorthand character classes

ok lets get to examples
```
Examples 
let shorthand = /\w+/;
let numbers = '42';
shorthand.test(numbers); // will return true
numbers.match(shorthand); // will return '42'
```
Match Everything But Letters and Numbers

So the exact opposite of what we did above is using the shorthand character \W let's see it in action
```
let shorthand = /\W+/;
let numbers = 42;
shorthand.test(numbers); // will return false
numbers.match(shorthand); // will return null
```

Match All Numbers 

Similarly on what we did above we can use the shorthand character , `\d` which is digits

Match All Non-Numbers

Similarly on what we did above we can use the shorthand character, `\D` which is non-digits

Match Whitespace 

Similary again on what we did above we can use the shorthand character, `\s` which will match whitespaces

Match Non-Whitespace Characters

Again another similar on what we did above we can use the shorthand characfter `\S` which will match non-whitespaces

Check for All or None

So here we are using again the ? character which states that because it is lazy matching
the character before the ? character is considered to be optional

```
Example
let american = "color";
let british = "colour";
let rainbowRegex= /colou?r/;
rainbowRegex.test(american); // Returns true
rainbowRegex.test(british); // Returns true
Which we can see that letter u is optional 
```
Positive and Negative Lookahead

Lookaheads are patterns that tell javascript to look-ahead in your string to check for patterns
further along. This can be useful when you want to search for multiple patterns over the same string

There are two kinds of lookaheads: `positive lookahead` and `negative lookahead`.

Differences is 
Positive
- will look to make sure the element in the search pattern is there but won't actually match it
Negative
- will look to make sure that the element is NOT there

for example we want to match something not followed by something else we can use the negative lookahead

Lookaheads are confusing so lets get some example
```
Example:
// Positive lookahead
let password = "abc123";
let checkPass = /(?=\w{3,6})(?=\D*\d)/;
checkPass.test(password); // Returns true
// Negative lookahead
let quit = "qu";
let noquit = "qt";
let quRegex= /q(?=u)/;
let qRegex = /q(?!u)/;
quit.match(quRegex); // Returns ["q"] see we want q to be followed by u but we dont want it to be matched along
noquit.match(qRegex); // Returns ["q"] it sees that there is no u so it returns q
```

Reuse Patterns Using Capture Groups

Sometimes you will search for a string that will occur multiple times and doing it manually
is wasteful and tedious. 

And there is as better way to do it using Capture Group
To use Capture groups we use the parentheses ()

You put the regex pattern that will repeat between the parentheses to specify where that repeat string will appear use the backslash (\) and then a number.

This number starts at 1 and increases with each additional capture group you use. An example would be \1 to match the first group.

The example below matches any word that occurs twice separated by a space:

```
let repeatStr = "regex regex";
let repeatRegex = /(\w+)\s\1/;
repeatRegex.test(repeatStr); // Returns true
repeatStr.match(repeatRegex); // Returns ["regex regex", "regex"]
```

### Debugging


