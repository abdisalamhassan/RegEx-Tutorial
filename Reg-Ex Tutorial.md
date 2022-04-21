# Become a regular with RegEx!

To begin lets start with the term Regex and what it stands for.RegEx is short for 'Regular Expressions'. A regex is a string of text(which can include letters,numbers and charactars).


 

## Summary

RegEx can help us sift through lots of data by finding the exact text that we ar looking for. Lets say you're looking through postal codes for a city. This list of data would would daunting to look through. But what if you knew what the postal code started with you could use that to aid your search using regex. You would match the information you hav with the information your looking for.

Regex is used in a plethora of languages such as:
 -Java
 -Python
 -Ruby
 -Javascript
 -PHP


for our tutorial tutorial today we will be working with the regular expression: \b4[0-9]{12}|(?:[0-9]{3})?\b. Other examples will be sprinkled in to make help us.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors in boats are devices that are attached on bots that are heavy weights used by captains to connect to the seabed below to stop the boat from moving.

That same logic applies to anchors in regex. They can let a user specify that you want to match digit in a specific spot in a line of text. It is important to know that not all anchors are created equal. The are string anchors, line anchors and attempt anchors.

- String anchors include the caret syntax(^) and the dollar syntax($). The carter syntax matches the start of the regex string, whereas the dollar syntax matches the end of the regex sting.

So in the following sting (password123) the ^ would match with the letter 'p' and the $ would match with the number '3'

- Line anchors operate a little diffrent. Lets make a new string(password\123). The caret(^) syntax matches after each line break *IN ADDITION* to matching with the start of the string. So from (password\123) it would match 'p' and '2'.

-Now reverse that logic for the dollar($) syntax. In the 'password\123' where would the match apply?
   -if you said 'd' and '3' you are right!

Now lets look back at the 

### Quantifiers

Looking at the name 'Quantifiers' itself gives us a clue as to what they do. To quantify something means to count it. So in this context quantifiers mean that a pattern shows up a certain number of times. Lets take a look at the diffrent types of quantifiers: 

- ('+"): This quantifier matches the pattern 1 or more times

- ('*"): Here it matches the pattern 0 or more times.

- ('?'): This matches its pattern zero or one times

- ('{n}'): This would match for exactly the n value. If 'n' is 4 then it would match 4 times

- ('{m,n}'): This provides a range. It would match for 'm' to 'n' number of times

- ('{n,}'):This would match for n or more number of times.


Now looking at our example from the beginning of this tutorial (\b4[0-9]{12}|(?:[0-9]{3})?\b) where would the quantifier be?

If you said {12} and {3} then you are right! You're doing great! Lets keep going.

### OR Operator

Have you ever grabbed dinner who is very pick and doesn't like when their food on the plate touches? Who hasn't! Now we don't have a spoon or fork when we write regular expressions so how can we work with 2 distinct groups?

We can use OR Operator's for that. Now in the example above(\b4[0-9]{12}|(?:[0-9]{3})?\b) there is a '|' character known as a vertical line or pipe. This work as sort of a curtain between the 2 groups. SO where one former group will return {12} matches, the latter will return {3}


### Character Classes

Just like in grade school there are diffrent classes each with diffrent rules, teachers and expectations.

Here with regex there are diffrent operators for diffrent classes that can help with matching.

- "\d": matches a single digit character

- "\D": matches a single *non-digit* character

- "\w": matches a word character

- "\W": matches a non-word character

- "\s": matches a whitespace character

- "\S": matches a *non-whitepace* character

- ".": matches any character


### Flags

Flags are parameters that help the scope of our search. These are the  diffrent types of flags:

- "g": This is a global search which is the largest scope  we which we can look through.

- "m": Multiline, this makes " ^ " and " $ " match the start and end of a line, instead of the whole string

- "i": insensitive, this makes the whole expression case-sensitive




### Grouping and Capturing

Grouping unifies a pattern or string so that it is matches in a complete block. These are some examples of grouping:

- "()": Creates a capture group.

- "(?:)": This disables the capturing group.

- "(?<>): Names the group by using whatever term is between the <>.


### Bracket Expressions

Bracket Expressions are characters that are enclosed by '[]' matching a single character the brackets. The following are some examples:

- '[]': matches any single character within the brackets

- '[]%': matches the string inside the brackets before the '%'

- Note: special characters, such as ? do not work within the brackets.

### Greedy and Lazy Match

Greed might not always be a good trait within a person but it can be helpful when it comes to reguar expressions. 

Do you remember the ? quantifier discussed earlier? Well the single '?' is considered greedy as it will match as many occurences of the given patterns as possible. 

Now a lazy match would use '??' and this would match as few ocurences of said pattern as possible.

### Boundaries

There are a couple types of boundaries each serving a diffrent purpose. They go as follows:

- "Word Boundary(\b)": This matches positions where one side is a word character(can be a letter,digit or underscore) and the other side in *not* a word character


- "Not-A-Word-Boundary(\B): This is the opposite of a word boundary. It will match when neither side a word character or when both sides are a word character



### Back-references

Back-refrences are used to match the same text previously matched by a capturing group. Lets look at some examples below:

- "([abc]\1): Using \1 it matches the same text that was matched by the first capturing group 

- "([abc])
  "([de]\2\1): this matches the same text that was matched by the second capturing group

  - "(?<bike>[xyz])\k<bike>":  this names the group 'bike' then refrences it later

### Look-ahead and Look-behind

Lookahead and lookbehind(also known lookaround) are zero-length assertations that are similair to [Anchors](#anchors) that we discussed above.

The diffrence is that the lookaround matches characters and provides a result (match or no match). Lets take a peek at some examples:

- "(?=)"
  "a(?=b): this matches an *a* only if it is *b* 

- "(?!r)"
  "a(?!b): this matches an *a* only if it is NOT followed by a *b*


## Author

Tutorial courtesy of Abdi Hassan (https://github.com/abdisalamhassan?tab=repositories)
