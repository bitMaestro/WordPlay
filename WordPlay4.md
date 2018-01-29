
__Palindrome Problem__

What is the longest palindrome word?  *A word that is spelled the same forwards and backwards.*

__Solution__



```python
word = 'apple'
word[0]
```




    'a'




```python
word[-1]
```




    'e'




```python
"""
Use range function to iterate the...
length of the word and print the indicies.
"""
for index in range(len(word)):
    print(index)
```

    0
    1
    2
    3
    4



```python
# word = 'radar'
word = 'apple'
is_palindrome = True
for index in range(len(word)):
    if word[index] != word[-(index + 1)]:
        is_palindrome = False
print(is_palindrome)
```

    False



```python
import scrabble



```python
longest = ""

for word in scrabble.wordlist:
    is_palindrome = True
    for index in range(len(word)):
        if word[index] != word[-(index + 1)]:
            is_palindrome = False
    if is_palindrome and len(word) > len(longest):
        longest = word
        
print(longest)
```

    rotavator


_The solution above work, however its a little complicated.  There is a_ ```reversed``` _method in Python we can noddle around with._


```python
word = 'apple'
list(reversed(word))
```




    ['e', 'l', 'p', 'p', 'a']




```python
list(word) == list(reversed(word))
```




    False




```python
word = 'radar'
list(word) == list(reversed(word))
```




    True




```python
longest = ""

for word in scrabble.wordlist:
    if list(word) == list(reversed(word)) and len(word) > len(longest):
        longest = word

print(longest)
```

    rotavator


_With_ ```reversed``` _we managed to write a more concise script.  Can we make it more concise?


```python
import string
string.ascii_lowercase[0:25]
```




    'abcdefghijklmnopqrstuvwxy'




```python
string.ascii_lowercase[0:15]
```




    'abcdefghijklmno'




```python
string.ascii_lowercase[::-1]
```




    'zyxwvutsrqponmlkjihgfedcba'




```python
word = 'rotavator'
word == word[::-1]
```




    True




```python
longest = ""

for word in scrabble.wordlist:
    if word == word[::-1] and len(word) > len(longest):
        longest = word
print(longest)
```

    rotavator


__Wow!!!__

By importing ```string``` we were able to slice and dice characters.  In particular ```string``` has a method that prints the reverse of and _ascii_ string.  This creates a beautiful syntax that's totally Pythonic.
