# find_node_in_graph_BFS

### Problem
Given a starting node in a graph and a target, traverse the graph using BFS and return true if a node with the target value exists, and false otherwise.
You may assume this graph is implemented via a Node class data structure:
```
class GNode {
  constructor(value = 0, children = []) {
    this.children = children
    this.value = value
  }
  
  hasPathTo(node) {
      // Write your code here.
  }
}

// Test Cases
var node2 = new GNode(2)
var node1 = new GNode(1, [node2, new GNode(3)])
var node4 = new GNode(4, [node1])
var node5 = new GNode(5, [node1, node4])
var node6 = new GNode(6)
var node7 = new GNode(1)
var node8 = new GNode(2)
var node9 = new GNode(3)
node7.children = [node8]
node9.children = [node7]
test.startProblem("Graph Search")
test.test(true, node5.hasPathTo(node2), 1)
test.test(false, node6.hasPathTo(node1), 2)
test.test(false, node1.hasPathTo(node4), 3)
test.test(true, node7.hasPathTo(node9), 4)
test.test(false, node7.hasPathTo(node1), 5)
test.endProblem()
```
