README.md

========================

DATA STRUCTURES:
(in Ruby)

========================

#BFS 

```
queue = [ root ]
until queue.empty?
    el = queue.shift
    process!(el) #return if it's 7 or else skip it
    el.children.each { |child | 
    queue << child }
end
```

#DFS ( Depth First Search ) # uses a stack

```
def dfs ( root, target )
    return nil if root is nil 
    return root if root.val == target
    root.children.each do |child |
        search_result = dfs( child, target )
        return search_result 
    end
    nil

end
```

base case:  

root.nil? false # or return nil if you didn't find something

root.val == target # root

# if I dfs on the left side or right side 
# person is on the left side


```
def dfs ( root, target )
    return nil if root is nil 
    return root if root.val == target
    root.children.each do | child | 
        search_result = dfs ( child, target ) # a node with the value three
        return search_result unless search_result.nil?
    end
    nil
end
```

root.nil? 
root val == target == root

```
def dfs ( root, target ) 
    return nil if root is nil
    return root if root.val == target
    root.children.each do | child |
      search_result == dfs ( child, target ) 
      return search_result unless search_result.nil?
    end
    nil
end
```

LIFO ( last-in-first-out )
1 2 3 4 5

( pop ), ( stack )

3.
DFS
"find value 6 in the graph above"
4 3 7 8 6 === 9? 5 1

