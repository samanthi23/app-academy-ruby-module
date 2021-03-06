```
class PolyTreeNode
   def initialize(value)
      @value = value # getter to get value outside of this class, instance variable
   end
   
=begin
#initialize(value) method that sets the value
parents = nil
children = []
=end
      
      
      
=begin      
      @value = value
      # value = [key, value]
      #parent = nil
      parent = nil
      #children = []
      children = []
=end
      
   end 
   
   def parent()
       # returns parent node
       # parent = parent.first
       @parent
   end
   
    
    
end
```

ADT
Set 

```
include?
>> 
delete
```

is a set shovel in 3 [3, # then shovel in "hello"]

is a set, unique. [2, "hello"]

iterate over the set to delete it or to do anything to it 

## uses a stack DFS so use recursion

base case: ```root.nil?``` then there is no tree it is an empty tree so return false or return nil

parameters root, target 

if the root is equal to the target

```root.val == target ```

in search

### base case is

then return the root ``` if( root.val == target) return root ```

``` def dfs(root, target) ```

1. if tree is nil
2. or if searching for target element in tree, match the element or return the thing

### left sub - tree contains the element

ask right sub-tree do you contain the element target I'm looking for?

no you don't

left sub-tree do you contain the element I'm looking for?

no you don't 

and parent is also not target

then there is no way that element in contained in this tree

but if in left sub-tree and it returned the element

then you can say "aha, it was in the left sub tree"

### inductive step

dfs on the left side ( using recursion ) or dfs on the right side ( using recursion )

``` left.dfs``` or ```right.dfs```

these two thing will tell us if it's ( the element ) is there

1. root
2. left sub tree
3. right sub tree

now we just have to ask the left sub tree and the right sub tree if they own this person that we are searchng for

for PolyTree and not a binary tree use ``` root.children```

#### this is peuso-code: 

``` 
root.children.each do |child|
 search_result = dfs(child, target) 
 return search_result unless search_result.nil?
end

nil
```

dfs(child, target), pass the target in

dfs(child, target), is recursion

children are an empty array [] if root nil

then whole thing should return nil if nothing

# parent= 

1. setter, sets the parent property
2. defining a setter method inside the class allows it to be set outside the class
```
def name=(name) #setter method
    @name = name
end
```

#### getters and setters:
1. sets the parents property

##### setter method

```
def name=(name) #setter method
    @name = name
end
```

```
def parent=(value)
    @parent = value
end
```

2. adds the node to their parent's array of children
3. unless setting the parent to nil

# notes

PolyTree : 

a, b, c, d, e

# b node

children of root node a is b, c, left subtree

and d right sub tree

value a

a's parent is nil

children of a is b, c, d or [b, c, d] array

child is a node or |child| in root.children.each do |child| 

current value is b node

b's children are []

b's parent is a node

## now think of it as a left sub-tree and a right sub-tree

left tree is b, c

right tree is d, d's child is e

## draw stack frame or stack diagram

a then b then c, left sub tree

first child is 4 so stack frame is 1, 2, 4. 

4.each.chidren will return a [] then the whole thing will return nil

4 pops off stack and passes down nil to the 2

2 goes down to 4 then it goes back up then it goes to 5 now ( 5 is 2's child )

```
class PolyTreeNode
  # ...
  # ...
  def inspect
    @value.inspect
  end
end
```

```
class PolyTreeNode
  # ...
  # ...
  def inspect
    { 'value' => @value, 'parent_value' => @parent.value }.inspect
  end
end
```

# think of it as a Abstract Data Type

use self method

and ._children method

left sub - tree and right sub - tree

detach from current parent

unless parent is nil node1.parent is 1

## self in Ruby

if parent node return then parent node is set

```
def coffee
  puts self
end

coffee
# main
```

```
class Salad
  def initialize
    @ingredients = []
  end
  def add_nuts
    @ingredients << :nuts
    self
  end
end
my_salad = Salad.new.add_nuts
```

## ._children

self.parent._chidren << self unless self.parent.nil?

variables can be _ underscore


# pseudo-code

1. check if parent nil if so no tree so return

2. detach from current parent

if self is a parent detach or delete self or delete node

3. set parent node to value passed in

4.  adds node to their parent's array of children ( unless we're setting parent to nil )

5. return self or node 

# parent=(parent)

parent=(parent) not parent=(value)

write a parent= method that sets the parent property

parent=(parent)

# @children.dup

copy an Object in Ruby

Duplicate

shallow copy

could also use ```deep_dup``` method for non-shallow copy

@children.dup

# def _children

```
protected # to give node direct access to another node's children
    

def _children
   @children
end
```



