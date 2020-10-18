objects that hold recursive references to other objects

1) PolyTreeNode#parent= does not add the same node twice
     Failure/Error: expect(node1.children).to eq([node2, node3])

       expected: [#<PolyTreeNode:0x007f8092bbc0f0 @parent=#<PolyTreeNode:0x007f8092bbc078 @parent=nil, @children=[#<PolyTreeNode:0x007f8092bbc0f0 ...>, #<PolyTreeNode:0x007f8092bc7f90 @parent=#<PolyTreeNode:0x007f8092bbc078 ...>, @children=[], @value="child2">, #<PolyTreeNode:0x007f8092bc7f90 @parent=#<PolyTreeNode:0x007f8092bbc078 ...>, @children=[], @value="child2">], @value="root">, @children=[], @value="child1">, #<PolyTreeNode:0x007f8092bc7f90 @parent=#<PolyTreeNode:0x007f8092bbc078 @parent=nil, @children=[#<PolyTreeNode:0x007f8092bbc0f0 @parent=#<PolyTreeNode:0x007f8092bbc078 ...>, @children=[], @value="child1">, #<PolyTreeNode:0x007f8092bc7f90 ...>, #<PolyTreeNode:0x007f8092bc7f90 ...>], @value="root">, @children=[], @value="child2">]
            got: [#<PolyTreeNode:0x007f8092bbc0f0 @parent=#<PolyTreeNode:0x007f8092bbc078 @parent=nil, @children=[...], @value="root">, @children=[], @value="child1">, #<PolyTreeNode:0x007f8092bc7f90 @parent=#<PolyTreeNode:0x007f8092bbc078 @parent=nil, @children=[...], @value="root">, @children=[], @value="child2">, #<PolyTreeNode:0x007f8092bc7f90 @parent=#<PolyTreeNode:0x007f8092bbc078 @parent=nil, @children=[...], @value="root">, @children=[], @value="child2">]

expected: / got:

```
class PolyTreeNode
  # ...
  # ...
  def inspect
    @value.inspect
  end
end
```

1) PolyTreeNode#parent= does not add the same node twice
   Failure/Error: expect(node1.children).to eq([node2, node3])
```
     expected: ["child1", "child2"]
          got: ["child1", "child2", "child2"]
   
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

1) PolyTreeNode#parent= does not add the same node twice
     Failure/Error: expect(node1.children).to eq([node2, node3])

       expected: [{"value"=>"child1", "parent_value"=>"root"}, {"value"=>"child2", "parent_value"=>"root"}]
            got: [{"value"=>"child1", "parent_value"=>"root"}, {"value"=>"child2", "parent_value"=>"root"}, {"value"=>"child2", "parent_value"=>"root"}]

Overriding inspect isn't always necessary, and you won't do it in every

