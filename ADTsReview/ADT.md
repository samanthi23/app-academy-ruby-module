# DATA STRUCTURES in Java but in App Academy's Ruby instead.

Harvard's Data Structures class Fall 2015.

# ADT

Set, is a collection of Objects. Unique keys-values ["a" => "apple", "b" => "boy", "c" => "cat"]
definition of set, Abstract Data Type. 3 defining properties

``` 
include?
<<
delete
```

# How would you implement a set 

1. check for inclusion
2. put things into it
3. and delete from it

# code 
1. to check for inclusion just iterate everything in the set
2. 
3. to delete something just iterate over the Set to delete something and just delete it
be careful of is that don't include duplicates iterate then make sure that thing is not included in the set
use 

# Map.rb
```
    def get(key)
```

 |ele| 
```
 pair_index = underlying_array.index { |pair| pair[0] == key }
```

## .index
```
a = [ "a", "b", "c" ]
a.index("b")              #=> 1
a.index("z")              #=> nil
a.index {|x| x == "b"}    #=> 1
``` 
ruby docs returns index of 

review Data Structures lectures @ Harvard. 

returns value 
```
array[0][1] if array[0] == key

```

array[key][value] if [array[0] == key]

```
array[0][1] == value
```

array[key][value] == value

else returns 
```
nil
```
not found
```
underlying_array.each { | ele | returns ele[1] if ele[0] == key }
nil
end
```

underlying_array.each { | element | returns element[value] if [element][0] == key
