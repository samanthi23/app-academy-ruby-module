# DFS

if root nil return

if root value is target return the root # base case

check left sub-tree

check right sub-tree

# think recursively

return node 2

node 2 is a root node of the left sub-tree

make that recursive call right away and store it in a variable the number of occurences in the rest of the string

``` int numOccurInRest = numOccur(ch, str.substring(1)); ```

``` return 1 + numOccurInRest```

``` 
else
   return 0 + numOccurInRest
```

building from the base case 

with recursion you don't want a counter

walking down the string character by character

stack frame: return 0 "", return 1 + 0 "a", return 1"ha", return 1 + 1 "aha"

numOccur('a', 'aha')
   
if the first character in this string is an 'a'

if "no" then return the number of occurences in the rest

returns 0, 1,1,2 "aha" returns 2


