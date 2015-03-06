# Graph
1)	You will create a directional Graph class that reads in a set of Nodes provided by the user.
2)	After you read in the Graph, the user will make various requests using 0-indexed values to refer to the Nodes:
a.	“find x y”, starting at Node x, is there a path to Node y.
b.	“distance x y”, starting at Node x, what is the distance (any valid distance, does not have to be shortest) to Node y. Return -1 for no path.
c.	“length”, returns how many Nodes exist.
d.	“add”, adds a new Node that is not connected to anything.
e.	“connect x y length”, connects Node x to Node y with the given length. Does not connect Node y to Node x. If a path already exists, this overwrites it.
f.	“remove x”, removes Node x from the Graph, returns true is able, false otherwise.
i.	while(“remove 0”) must be able to empty the Graph.

User Input Specification:
The user will first enter a word to indicate what type of input you are getting: “matrix”, “list”, “node”.
The user will then enter a number to tell you how many Nodes exist in your graph. After that, they will enter in the Nodes based on the type of input.
	Matrix: The user will enter in all of the values for an adjacency matrix where -1 indicates no connection and all distances are greater than 0. The connection between a Node and itself will always be 0.
	List: The user will enter the id for the current Node, starting at 0, and then the number of connections that Node has. For each connection, the user will enter the length of the connection and to which Node it is connected to.
	Node: The user will enter a number to tell you how many connections exist. For each connection, the user will enter three numbers, the source Node, destination Node and the distance.

Sample Inputs:
Matrix:
matrix 5
0 1 2 3 4
3 0 4 2 1
3 4 0 5 5
6 5 2 0 -1
1 2 3 4 0

List:
list 5
0 4 1 1 2 2 3 3 4 4
1 4 3 0 4 2 2 3 1 4
2 4 3 0 4 1 5 3 5 4
3 3 6 0 5 1 2 2
4 4 1 0 2 1 3 2 4 3

Node:
node 5
19
0 1 1
0 2 2
0 3 3
0 4 4
1 0 3
1 2 4
1 3 2
1 4 1
2 0 3
2 1 4
2 3 5
2 4 5
3 0 6
3 1 5
3 2 2
4 0 1
4 1 2
4 2 3
4 3 4
