
__Problem__

Are there any words in the scrabble dictionary that do not contian reoccuring letters, or double letters in a single word?




```python
import scrabble
import string
```


```python
for letter in string.ascii_lowercase:
    exists = False
    for word in scrabble.wordlist:
        if letter * 2 in word:
            exists = True
            break
    if not exists:
        print("There are no English words with a double " + letter)
        
```

    There are no English words with a double q
    There are no English words with a double x



```python
for letter in string.ascii_lowercase:
    exists = False
    for word in scrabble.wordlist:
        if letter * 2 in word:
            exists = True
            break
    if not exists:
        print("There are no Englisgh words with a bouble " + letter)
```

    There are no Englisgh words with a bouble q
    There are no Englisgh words with a bouble x



```python

```
