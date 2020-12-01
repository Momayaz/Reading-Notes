# Regex tutorial:
## There three methods that relate to Regex:
1. Basic method:

Anchors — ^ and $ which matches the first and last and the middle strings.

```
^The        matches any string that starts with The -> Try it!
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it
```
2. Intermediate topics:
operator is very useful when we need to extract information from strings or data using your preferred programming language. Any multiple occurrences captured by several groups will be exposed in the form of a classical array: we will access their values specifying using an index on the result of the match.
If we choose to put a name to the groups (using (?<foo>...)) we will be able to retrieve the group values using the match result like a dictionary where the keys will be the name of each group.

3. Advanced topics:
```
\babc\b  performs a "whole words only" search -> Try it!
\b represents an anchor like caret (it is similar to $ and ^) matching positions where one side is a word character (like \w) and the other side is not a word character (for instance it may be the beginning of the string or a space character).
```
It comes with its negation, \B. This matches all positions where \b doesn’t match and could be if we want to find a search pattern fully surrounded by word characters.
________________
# Grid;
grid is so important and comfortable to deal with in order to divide the bage and make the element inside look perfect. We have a lot of grid commands that related to columns and row, we can divid the bage into fraction using ```grid-template-culomns: then the number of fractions that you want to divide. The same pattren to row.
_______
# Responsive Layouts with CSS Grid:
Resposive layout used in order to make the bage that you made flexiable, i mean when you zoom in or zoom out, the bage by using 'Resposive layout' will transform automatically. Resposive layout works along side with Css Grid, as we should to make the bage as columns and rows by using Grid and using ```@media``` of responsive layout.
