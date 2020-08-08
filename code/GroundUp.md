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

### 4. Find the first 100 prime numbers: 2, 3, 5, 7, 11, 13, 17, 

```Clojure
(defn divisible? [x y] (= (rem x y) 0))
(defn prime? [n]
  (not-any? #(divisible? n %) (range 2 n)))
(take 100 (filter prime? (iterate inc 2) ))
```

I was really stumped on this one so looked for a solution and worked through it step by step to understand what was happening.
