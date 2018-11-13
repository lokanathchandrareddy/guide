---
title: Truncate a String
---
![:triangular_flag_on_post:](https://forum.freecodecamp.com/images/emoji/emoji_one/triangular_flag_on_post.png?v=3 ":triangular_flag_on_post:") Remember to use <a>**`Read-Search-Ask`**</a> if you get stuck. Try to pair program ![:busts_in_silhouette:](https://forum.freecodecamp.com/images/emoji/emoji_one/busts_in_silhouette.png?v=3 ":busts_in_silhouette:") and write your own code ![:pencil:](https://forum.freecodecamp.com/images/emoji/emoji_one/pencil.png?v=3 ":pencil:")

### ![:checkered_flag:](https://forum.freecodecamp.com/images/emoji/emoji_one/checkered_flag.png?v=3 ":checkered_flag:") Problem Explanation:

We need to reduce the length of the string or **truncate** it if it is longer than the given maximum lengths specified and add `...` to the end. If it is not that long then we keep it as is.

#### Relevant Links

*   <a href='https://github.com/FreeCodeCamp/FreeCodeCamp/wiki/JS-String-Prototype-Slice' target='_blank' rel='nofollow'>String.prototype.slice()</a>

## ![:speech_balloon:](https://forum.freecodecamp.com/images/emoji/emoji_one/speech_balloon.png?v=3 ":speech_balloon:") Hint: 1

Strings are immutable in JavaScript so we will need a new variable to store the truncated string.

> _try to solve the problem now_

## ![:speech_balloon:](https://forum.freecodecamp.com/images/emoji/emoji_one/speech_balloon.png?v=3 ":speech_balloon:") Hint: 2

You will need to use the slice() method and specify where to start and where to stop.

> _try to solve the problem now_

## ![:speech_balloon:](https://forum.freecodecamp.com/images/emoji/emoji_one/speech_balloon.png?v=3 ":speech_balloon:") Hint: 3

Do not forget that when we truncate the word, we also must count the length added by `...`

> _try to solve the problem now_

## Spoiler Alert!

![warning sign](//discourse-user-assets.s3.amazonaws.com/original/2X/2/2d6c412a50797771301e7ceabd554cef4edcd74d.gif)

**Solution ahead!**

## ![:beginner:](https://forum.freecodecamp.com/images/emoji/emoji_one/beginner.png?v=3 ":beginner:")  Code Solution:

    function truncateString(str, num) {
    // Clear out that junk in your trunk
    if (str.length > num ) {
        return str.slice(0, num) + '...';
        } else {
        return str;
        }
    }

![:rocket:](https://forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=3 ":rocket:") <a href='https://repl.it/CLjU/55' target='_blank' rel='nofollow'>Run Code</a>

### Code Explanation:

*   First we start off with a simple `if` statement to check if the length of the string is greater than the given maximum string length (second argument) - num.
*   If our string length is greater than the `num` we want to truncate and return a slice of our string starting at character 0, and ending at given maximum string length (second argument) `num`. We then append our `'...'` to the end of the string.
*   Finally, if it is false, it means our string length is less than our truncation i.e given maximum string length (second argument) `num`. Therefore, we can just return the string without the `'...'`.

## ![:rotating_light:](https://forum.freecodecamp.com/images/emoji/emoji_one/rotating_light.png?v=3 ":rotating_light:") Advanced Code Solution:

    function truncateString(str, num) {
        // Clear out that junk in your trunk
        return (str.length <= num) ? str : str.slice(0, num) + '...'; 
    }

![:rocket:](https://forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=3 ":rocket:") <a href='https://repl.it/CLjU/54' target='_blank' rel='nofollow'>Run Code</a>

### Code Explanation:

*   We use a ternary operator to check the condition `(str.length <= num)` is true or not. Here the condition is to check if the length of the string is lesser than or equal to the given maximum string length (second argument) - num.

*   If it is true then the first block is executed, i.e. we just return the original string.

*   If it is false, then the second block is executed i.e we truncate and return a slice of the string with starting at the 0 and ending at given maximum string length (second argument) `num`. Then we concatenate `'...'` at the end of the sliced string.  

*   **NOTE** In order to understand the above code, you need to understand how a Ternary Operator works. The Ternary Operator is frequently used as a shortcut for the `if` statement and follows this format: `condition ? expr1 : expr2`. If the `condition` evaluates to true, the operator returns the value of `expr1`. Otherwise, it returns the value of `expr2`.

#### Relevant Links

*   <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator' target='_blank' rel='nofollow'>Conditional (ternary) Operator</a>
*   <a href='https://github.com/FreeCodeCamp/FreeCodeCamp/wiki/JS-String-Prototype-Slice' target='_blank' rel='nofollow'>String.prototype.slice()</a>

## ![:clipboard:](https://forum.freecodecamp.com/images/emoji/emoji_one/clipboard.png?v=3 ":clipboard:") NOTES FOR CONTRIBUTIONS:

*   ![:warning:](https://forum.freecodecamp.com/images/emoji/emoji_one/warning.png?v=3 ":warning:") **DO NOT** add solutions that are similar to any existing solutions. If you think it is **_similar but better_**, then try to merge (or replace) the existing similar solution.
*   Add an explanation of your solution.
*   Categorize the solution in one of the following categories — **Basic**, **Intermediate** and **Advanced**. ![:traffic_light:](https://forum.freecodecamp.com/images/emoji/emoji_one/traffic_light.png?v=3 ":traffic_light:")
*   Please add your username only if you have added any **relevant main contents**. (![:warning:](https://forum.freecodecamp.com/images/emoji/emoji_one/warning.png?v=3 ":warning:") **_DO NOT_** _remove any existing usernames_)

> See ![:point_right:](https://forum.freecodecamp.com/images/emoji/emoji_one/point_right.png?v=3 ":point_right:") <a href='http://forum.freecodecamp.com/t/algorithm-article-template/14272' target='_blank' rel='nofollow'>**`Wiki Challenge Solution Template`**</a> for reference.
