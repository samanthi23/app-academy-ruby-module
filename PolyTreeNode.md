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






