# 4Clojure

## 1. Nothing but the Truth 

```clojure
true - although `(not false)` also seems to work, interesting.
```

## 2. Simple Math

```clojure
4
```

## 3. Intro to Strings

```clojure
"HELLO WORLD"
```

## 4. Intro to Lists

```clojure
:a :b :c - man these brackets and semi columns will take some getting used to
```

## 5. Lists: conj

```clojure
'(1 2 3 4) - hmm interesting, conj takes the last item and adds it to the fron of the list.
```

## 6. Intro to Vectors

```clojure
:a :b :c - similar to the lists point, intersting, vectors and lists - need to research further what is exact difference
```

## 7. Vectors: conj

```clojure
'(1 2 3 4)
```

## 8. Intro to Sets

```clojure
#{:a :b :c :d}
```

## 9. Sets: conj

```clojure
2 - adds a character
```

## 10. Intro to Maps

```clojure
20 - returns the value of b
```

## 11.  Maps: conj

```clojure
[:b 2] - interestingly {:b 2} also works
```
 
 ## 12.  Intro to Sequences

```clojure
3 - returns the value of the specified position
```


## 13. Sequences: rest
```clojure
[20 30 40] - returns the sequence from the 1st item. Also '(20 30 40) is ok as this is interchangeable
```

## 14. Intro to Functions
```clojure
8 - wow so many differnt ways to get the same answer
```

## 15. Double Down
```clojure
(fn [x] (* x 2))
```


## 16. Hello World
```clojure
(fn [x] (str "Hello, " x "!"))
```

## 17. Sequences: map
```clojure
[6 7 8]
```

## 18. Sequences: filter
```clojure
'(6 7)
```

## 19. Last Element
```clojure
(fn [x] (nth x (- (count x) 1)))
```

## 20. Penultimate Element
```clojure
(fn [x] (nth x (- (count x) 2)))
```

## 21. nth Element
```clojure
#(first (drop %2 %1))
```
## 22. Count a Sequence
```clojure
(fn cnt [lst]
    (if (= lst nil)
        0
        (inc (cnt (next lst)))))
```
## 23. Reverse a Sequence
```clojure
#(reduce conj () %)
```
## 24. Sum It All Up
```clojure
#(reduce + %)
```
## 25. Find the odd numbers
```clojure
#(filter odd? %)
```
## 26. Fibonacci Sequence
```clojure

```

## 27. Palindrome Detector
```clojure
(fn [word]
  (if (string? word)
    (= (apply str (reverse word) word))
  	(= (reverse word) word)))
```

## 29. Get the Caps
```clojure
(fn [uppercase]
  (apply str (filter #(Character/isUpperCase %) uppercase)))
```

