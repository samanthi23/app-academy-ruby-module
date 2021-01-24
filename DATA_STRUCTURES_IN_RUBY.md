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
"really aggresively go to the leaves"
4, 5, 2, 6, 7, 3, 1



## if you only do these two operations then it is a queue
1. push / pop
2. unshift / shift

### if you ever violate the of the queue it will never work it must be FIFO, First in first out
# Trees

most common is a binary tree
has a directionality if it doesn't have that then it is not a Tree
1. at most two children
2. at most three chidren, ternary tree, three, and two, and one
## also there is a unary tree, at most one, a linked list

### for a tree that gives no guarantee about the number of children, nodes

also known as a PolyTreeNode
1. a ( root node ) is a subtree
2. b is the root of another subtree in PolyTreeNode

iterate over a tree how to and traverse tree, different tree traverals

## Sudoku

### Tic Tac Toe

see all possible, DFS or BFS or etc..

# 1, 2, 3, 4, 5, 6, 7
## layers
1, 
2 3, 
4 5 6 7 



all states of tic tac toe marks, X O 

we have to learn that how do you traverse a tree in different ways



