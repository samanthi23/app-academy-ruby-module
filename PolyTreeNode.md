```
class PolyTreeNode
   def initialize(value)
   
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
       # returns nodes parent
       parent = parent.first
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



