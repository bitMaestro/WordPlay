

```python
import scrabble
```

__Print all words containing 'uu'__

Check for every word in the scrabble text file and print any words that have 'uu' in the word. 


```python
for word in scrabble.wordlist:
    if 'uu' in word:
        print(word)
```

    busuuti
    busuutis
    carduus
    carduuses
    continuum
    continuums
    duumvir
    duumviral
    duumvirate
    duumvirates
    duumviri
    duumvirs
    individuum
    lituus
    lituuses
    menstruum
    menstruums
    mutuum
    mutuums
    muumuu
    muumuus
    paramenstruum
    paramenstruums
    residuum
    residuums
    squush
    squushed
    squushes
    squushing
    triduum
    triduums
    ultravacuum
    ultravacuums
    vacuum
    vacuumed
    vacuuming
    vacuums
    weltanschauung
    weltanschauungs



```python
# search for words with 9 characters

for word in scrabble.wordlist:
    if len(word) == 9:
        print(word)
```

    aardvarks
    aasvogels
    abactinal
    abamperes
    ...
   
   
   
    




```python
# search for words with only 2 characters.

for word in scrabble.wordlist:
    if len(word) == 2:
        if 'z' in word:
            print(word)
```

    za
    zo



```python
# what is the longest word in the dictionary?

longest = ""

for word in scrabble.wordlist:
    if len(word) > len(longest):
        longest = word
#print(longest, 
      
print('{} is the longest word in the dictionary with a lenght of {}.'.format(longest, (len(longest))))
```

    abiogenetically is the longest word in the dictionary with a lenght of 15.



```python
for word in scrabble.wordlist:
    if len(word) == 4:
        if 't' in word:
            print(word)
```

    abet
    abut
    acta
    acts
    adit
    airt
    ...
    zits
    zoot



```python

```
