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

### in a Hashmap just check for inclusion no need to iterate over everything

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

# Set 
this array implements an Abstract Data Type : "Set"

instead of using an Array I can use a hashmap, Hashmap or dictionary
with values set to true 

```
[ 3 => "true" ]
[ "hello" => "true" ]
```

## Hashmap

don't have to worry about duplicates because the Hashmap 
already takes care of that

```
[ 3 => "true" ]
[ "hello" => "true" ]
```

# return value is meant to check success or failure

return true - success

return false - failure, etc..

if ```item == null``` disallow that don't want people to store a null value in ArrayBag ADT

```throw new IllegalArgumentException()```

this and item in stack frame ```b.add(message)```

this, a copy of the reference

now we have 3 references to the string, item, message, and items[0]

# this

```
if (this.numItems == this.items.length)
return false;
else {
 this.items[this.numItems] = item;
 this.numItems++
 return true;
}
```

this field is coming from the called Object




