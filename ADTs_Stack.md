```
class Stack
    def initialize
      # create ivar to store stack here!
    end

    def push(el)
      # adds an element to the stack
    end

    def pop
      # removes one element from the stack
    end

    def peek
      # returns, but doesn't remove, the top element in the stack
    end
  end
```  

```
class Queue

  def enqueue(el)
     # adds an element to the queue
  end
  
  def dequeue
    # removes an element in the queue
  end
  
  def peek
    # returns, but doesn't remove, the top element in the stack
  end 

end
```

stores information in key-value pairs

my_map = [[k1,v1], [k2,v2], [k3, v2], ...]


Exercise 3 - Map

So set is unique keys ?


set - 
```

include? # check if it's in the set, check for inclusion

<< #push things into it 

delete # and delete from them

implement them with an Array

```

instead of using an Array I can use a hashmap
set key is 3 and => rocket to true
push 3 into Array
this Array can implement a Set is Unique, Abstract Data Type === ADT
public methods:
``` 
{ 3 => true } 
{ "hello" => true }

```


vocabulary : hashmap. no longer need to delete in a hashmap because a set is unique only so 

```
class Map

  def set(key, value) 
     # set method can be used to either create a new key-value pair 
     # or update the value of a pre-existing key
  end
  
  def get(key) 
  
  end
  
  def delete(key)
  
  end
  
  def show
     
  
  end 
end
```


