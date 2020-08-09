# Chapter 4
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



# Chapter 6
### 1. Use delay to compute this sum lazily; show that it takes no time to return the delay, but roughly 1 second to deref.

Start off with calculating time it takes to get to 1,000,000:

```Clojure
(defn sum [start end] (reduce + (range start end)))
(time (sum 0 1e7))
"Elapsed time: 188.5435 msecs"
=> 49999995000000
```

Added in the later delay 
```Clojure
(defn sum [start end] (reduce + (range start end)))
(time (def later (delay (sum 0 1e7))))
(time (deref later))
"Elapsed time: 0.1198 msecs"
"Elapsed time: 219.3157 msecs"
=> 49999995000000
```

### 3. If your computer has two cores, you can do this expensive computation twice as fast by splitting it into two parts: (sum 0 (/ 1e7 2)), and (sum (/ 1e7 2) 1e7), then adding those parts together. Use future to do both parts at once, and show that this strategy gets the same answer as the single-threaded version, but takes roughly half the time.

```Clojure
(time (let [a (future (sum 0 (/ 1e7 2)))
            b (future (sum (/ 1e7 2) 1e7))]
        (+ @a @b)))
"Elapsed time: 144.8362 msecs"
=> 4.9999995E13
```
