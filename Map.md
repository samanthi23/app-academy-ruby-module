Map.md

#2d array no idea 
    # implements a map using only arrays
    
    
```
=begin

A map is a 2d array
   - where the keys are always unique
   
   my_map = [[key1, value1], [key2, value2], [key3, value2], ...]
   
   set(key,value) # note that the set metohd can be used to either create a new key-value pair or update the value for a pre-existing key
   get(key), deletek(key), show
   
   - At its essence, a Map is just an unordered set of key-value pairs with unique keys
   - a hash map is just a specific way to implement a ADT of a Map
=end
```

```
=begin

map / dictionary
only need these 3 methods:
are set, get, delete

a hashmap is just a Set (unique keys ) of key value pairs, keys are unique, also called a dictionary 


=end
```

hello maps to world: 

```
["hello", "world" ]

```

and then I want to map 2 to 4:
nest key-value pairs together in tuples # MIT vocabulary word

```
[["hello", "world"], [2,4]]
```

this is implementing

``` 
hello => world
2 => 4

```

don't want to add a key-value pair I just want to add

a map have the following instance methods: set(key, value), get(key), delete(key), show
