# Regular Expressions
* Regular expressions are used to find certain words or patterns inside of strings.

### Finding the word "the" in the string "The dog chased the cat"
    /the/gi

* / is the start of the regular expression.

* the is the pattern we want to match.

* / is the end of the regular expression.

* g means global, which causes the pattern to return all matches in the string, not just the first one.

* i means that we want to ignore the case (uppercase or lowercase) when searching for the pattern.

### Finding Numbers with Regular Expressions
* We can use special selectors in Regular Expressions to select a particular type of value.

* One such selector is the digit selector \d which is used to retrieve one digit (e.g. numbers 0 to 9) in a string.

* In JavaScript, it is used like this: /\d/g.

* Appending a plus sign (+) after the selector, e.g. /\d+/g, allows this regular expression to match one or more digits.

* The trailing g is short for 'global', which allows this regular expression to find all matches rather than stop at the first match.

### Finding Whitespace with Regular Expressions
* We can also use regular expression selectors like \s to find whitespace in a string.

* The whitespace characters are " " (space), \r (the carriage return), \n (newline), \t (tab), and \f (the form feed).

* The whitespace regular expression looks like this:

    /\s+/g
