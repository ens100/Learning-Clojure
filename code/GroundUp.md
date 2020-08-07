# Chapter 3
### 1. Write a function to find out if a string is a palindrome–that is, if it looks the same forwards and backwards.

Here is how I acheived this bad boy:

- Started of with defining both words: ```(= ["oppo"] [(apply str (reverse "oppo"))])```

- Then added a function so that any word could be inputted: 
```Clojure 
(defn word
  [check]
  (= [check] [(apply str (reverse check))]))
  ``` 
Booom !

### 2.Find the number of ‘c’s in “abracadabra”.
```Clojure
((frequencies "abracadabra"))
```

To just find the "c"
```Clojure
((frequencies(seq "abracadabra"))\c)
```

This basically splits abracadabra into each letter and then frequency just counts c

### 3. Write your own version of filter.


### 4. Find the first 100 prime numbers: 2, 3, 5, 7, 11, 13, 17, 
