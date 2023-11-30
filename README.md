# Theorical foundation of Matrix, Graphs, and Trees #

--- This READ-ME document contains my annotations in matrices, graphs, and trees from my theoretical studies. I will add some of my Python exercises about those subjects in this repository. 


## __MATRIX__ ## 

**TRANSPOSITION** = is created by turning/swapping rows into columns and columns into rows.

m x 1 = column vector
1 x n = row vector

All matrix vectors without the transposition sign ARE COLUMN VECTOR... They will only be a row vector when it has the transposition sign.

**DIAGONAL MATRIX** = all elements outside the main diagonal are zero. The main diagonal can be any number, even zero. The all-zero matrix is a special type of diagonal matrix

**TRIANGULAR MATRIX** = is upper triangular if the upper part of the main diagonal is different than zero and the bottom is all zero ... end lower triangular otherwise.

**IDENTITY MATRIX** = is a Diagonal matrix where all elements in the main diagonal are = 1 and all others are =0.  Is denoted by E.

**SIMETRIC MATRIX** = If you transpose a matrix and it maintains the same ->  A = At. To be simetric the matrix must be square! Every square diagonal and all square Identy are symmetric.

**SKEW-SIMETRIC** =    A = -At

**ADITION OF MATRIX** = Just add elements of the same position.
IN ADDITION, THOSE LAWS APPLY:
*COMMUTATIVE: A+B= B+A
*ASSOCIATIVE: A+(B+C) = (A+B)+C
*ZERO MATRIX IS THE NEUTRAL ELEMENT IN ADDITION: A+0 = O+A = A


**SCALAR MULTIPLICATION** = It just multiplies each element of the matrix by a scalar (any real number different than zero). The following laws applied:
*COMMUTATIVE: x*A = A*x
*ASSOCIATIVE: (x*y)*A = x* (y*A)
*DISTRIBUTIVE: (x+y)*A = x*A+ y*A
or             x*(A+B) = x*A + x*B    
The neutral scalar is the number 1. The scalar 0 will return a zero matrix.
    

**DECOMPOSITION THEOREM** = ANY Square matrix A can be represented by the sum of A = B+C where B is symmetric and C is skew-symmetric of A.
symetric -------->  B= 0,5*(A+At)
skew-symmetric -->  C= 0,5*(A-At)

    
**DOT PRODUCT OF VECTORS** = If a row vector is multiplied by a column vector, and you multiply each corresponding index and add all results to another you will find out a real number = Scalar. It only applies to vectors with the same index. IN THIS CASE, COMMUTATIVE LAW APPLIES. at*b = bt*a. Distributive law too.


**MULTIPLICATION OF MATRICES** = The number of columns of the first must be the same as the number of lines of the second because the multiplication is: MULTIPLY EACH ROW ELEMENT OF THE FIRST WITH THE SAME COLUMN-INDEX ELEMENT OF THE SECOND AND SUM ALL RESULTS.
*Diagonal matrices (all zero except the main diagonal) play an important role in multiplication because depending on the order of the multiplication the main diagonal will alter the row or the columns of the matrix result.
    *LAWS OF MULTIPLICATION:
        - ASSOCIATIVE: (A*B)*C = A*(B*C)
        - DISTRIBUTIVE: A*(B+C) = A*B + A*C
        - IDENTITY:  A*E = A
        - ZERO MATRIX = O --> A*0 = 0
        - SCALAR MULTIPLICATION WITH AN IDENTITY MATRIX MULTIPLICATION:  x*A = (x*E)*A
        - POWER MATRIX CAN BE SIMPLIFIED:    A^s+t = A^s*A^t
                                              A^s*t = (A^s)^t
*THE NEUTRAL ELEMENT IN MATRIX MULTIPLICATION IS THE IDENTITY MATRIX. A*E = E*A = A
**ATTENTION**: commutative law generally does NOT apply to the multiplication of matrices because   A*B != B*A


**LAWS OF TRANSPOSITION**
* (At)t = A
* (A+B)t = At + Bt
* (x*A)t = x*At
* (A*B)t = Bt * At
* Et = E


**INVERSE/REGULAR MATRICES** = Every real number x other than zero has an inverse value = (x^-1), and when the inverse is multiplied by x the result must be = 1. The inverse can be found as    1/x = x^-1
**An inverse matrix MAY exist only for square matrices. Not every square matrix has an inverse.**
The multiplication of a matrix by its inverse = identity:   A*A^-1 = A^-1*A = E
IF THE INVERSE MATRIX EXISTS THE MATRIX IS CALLED INVERTIBLE OU REGULAR. If not if called non-invertible or singular.

**IF THE DETERMINANTE IS DIFFERENT THAN ZERO THAN THE MATRIX IS INVERTIBLE because it represents that the rows or columns of the matrix are linearly independent.**
**If the determinant = 0 then the matrix is NOT invertible.**

    1  2  3       1  2  3  | 1  2         the determinante is=   x-y
    4  5  6       4  5  6  | 4  5          1*5*9  + 2*6*7 + 3*4*8 = x
    7  8  9       7  8  9  | 7  8          3*5*7  + 1*6*8  + 2*4*9 = y

In 2x2 matrices to calculate the inverse (if the det != 0) just invert the order of the elements on the main diagonal and invert the sign (*-1) of the elements on the second diagonal. Divide each element of the matrix by the determinant (divide because is the inverse of the determinant that matters 1/det (multiplay 1/det is the same as directly dividing by the det.)
**An square diagonal matrix can be inverse if all elements of the main diagonal are !=0 and to invert you just need the invert each element of the main diagonal separately,** i.e., just put each one in the form of 1/x. 
A triangular upper or lower is also invertible if the main diagonal has NO zero element (if it has a zero the determinant will be also zero) so it is not invertible.
**GENERAL LAWS**:
- Inversion and transposition are interchangeable: (At)^-1 = (A^-1)t
- IF A is symmetric then A^-1 is also symmetric
- Shock-shoe rule:  (A*B)^-1 = B^-1*A^-1

**SIMETRICAL ENCRYPTION PROCEDURE** = multiply a message by a matrix to encrypt and multiply the result by the inverse of the matrix key to decrypt. 


**ORTHOGONAL MATRICES** = A square matrix is called ORTHOGONAL IF, AND ONLY IF A^-1 = At 
For a Orthogonal matrix A, At is also orthogonal... So ALSO APPLIES  A * At = A * A^-1 = E
IF the matrix is SIMETRIC = A * A = E

        

##__INTRODUCTION TO GRAPHS__##

**Graph**: A graph is a collection of vertices (or nodes) and edges that connect pairs of nodes. Graphs can be directed (edges have a direction) or undirected.

**EDGE**: A line that connects vertices (nodes) in a graph;

**UNDIRECTED Graph**: A graph in which edges do not have a specific direction;  G = ( V , E) with a set of finite nodes V={v1,v2,...vn} and set of edges E={e1,e2,...em}. V CAN NOT BE AN EMPTY SET, it needs at least one node. 

**DIRECTED GRAPH**: A graph in which each edge has a direction, indicating the order of connected vertices;

**ISOLATED NODE** = a node that is not connected to any other node by an edge.

**ADJACENT NODES / NEIGHBORS**: Nodes that are directly connected by the same edge. In a loop, the node is its own neighbor. 

**INCIDENT EDGE**: the edge that connects a node(s) in question. You say, edge E is incident to the node v1 and v2 ...

**PARALLEL EDGE or MULTIPLE EDGES**: Connect the same two nodes;

**LOOP**: the edge that connects a node to itself

**SIMPLE GRAPH**: NO parallel edges (multiple edges) and NO Loops.

**FINITE GRAPH**: A graph with a finite number of nodes and edges.

**INCIDENCE FUNCTION**: The node(s) that is/are connected to an edge. Write it as:   e1 |-> {v2, v4)  ; e2|-> {v5}loop

**DEGREE OF A NODE or VALENCE or NODE DEGREE**: the total of edges incident/connected to a node, or START in that node. Isolated nodes have a degree=0. Loops count 2. 

**REGULAR GRAPH** = a graph where every node has the same degree. An example is the Petersen graph where every node has degree 3, and can be called "regular of degree 3". 

**HANDSHAKING LEMMA**: Euler states that: In any FINITE AND UNDIRECTED AND SIMPLE graph the sum of all node degrees is twice the number of edges.
THEN THE SUM OF ALL NODES DEGREES MUST BE EVEN. And in every finite, undirected, and simple graph must exist at leat two nodes with the same degree.
Exemple is impossible to draw a graph with 7 nodes whet all nodes has degree 3 .. because de sum will be 21, an odd number.
Is also impossible to draw a graph with 4 nodes with the respective degrees (1,2,3,4) the sum is even, BUT is impossible because there must exist at least two nodes with the same degree.

**ISOMORPHIC GRAPHS**: Two graphs are called isomorphic if there exists a bijective mapping in each node. They contain the same number of nodes, edges, and degrees. But is necessary to make the mapping to guarantee the exact relation of connections, because a graph with the same number of nodes, edges, and degree could not be isomorphic.

**SUBGRAPH**: A graph formed by a subset of vertices and edges from a larger graph.

**PLANAR GRAPH**: A graph (that is or has an isomorphic representation) drawn on a plane without its edges crossing.

**FACES**: the areas divided by edges in a planar graph. The outside is also counted as 1 face.

**EULER'S POLYHEDRAL FORMULA**:  (vertices-edges+faces=2)            V - E + F = 2 
In any connected and planar graph, this formula is true.
????Using this formula you can find out if a graph can be planar???


**ADJACENCY MATRIX**: Can be used to compact representation of graphs. A matrix representing connections between vertices in a graph. The elements indicate whether there is an edge between vertices. Consider each node as an address in a sequence is rows and columns, and then the element Mij will be the number of edges that connect each address node. It can be 0 if no connection, 2 if it is an undirected loop or any in other cases.
THE ADJACENCY MATRIX OF AN UNDIRECTED GRAPH IS AWAYS SYMMETRIC (the information is duplicated between the triangular faces because both parts of the edge are counted). 
BUT, **THE ADJACENCY MATRIX OF A DIGRAPH IN GENERAL IS NOT SIMETRIC**, because it only represents the way the arrow goes. In digraph the sum of row vector=outputdegree and the sum of column vector=inputdegree.
In a SIMPLE GRAPH (no loops, no parallels) the adjacency matrix has all zeros in the main diagonal, and other Mij will be <=1.
The sum of a row or column vector shows the degree of the node in question. 
The sum of all elements of the matrix is twice the number of edges.


**DIRECTED GRAPH or DIGRAPH**: ALL edges have a direction/orientation. Here the incidence function shows the direction separated by a comma in an ordered pair (origin, destination).    e|-> (i, j) even in the case of a loop where i=j.  If you change the order of the ordered pair you change the graph!
Two edges with the same start and destination node (same i,j) are PARALLEL. But if the start and destination are opposite [ (i,j) and (j, i) they are ANTIPARALLEL or OPPOSITE.
-IN-DEGREE: the total of edges arriving in the node.
-OUT-DEGREE: the total of edges leaving the node.
*The total of all IN and OUT and edges must be equal. The SUM of both IN and OUT degrees is the total degree of a Digraph.
Each undirected graph CAN be converted into a DIGRAPH by the substitution of each edge by antiparallel edges and the loops replaced for just a directed edge.

**SHADOW**: is the opposite way, when you transform a Digraph in an Undirected graph replacing each directed edge with an undirected one.
*In the isomorphism of digraphs the direction of the arrow must also be respected.



##_SHORTES PATH PROBLEM - DIJKSTRA'S ALGORITHM_##

**WEIGHTED GRAPH** = have a mapping relation (also called weight function or cost function) that assigns a weight (value) for each edge.
The weight matrix has a value zero in the main diagonal because cost nothing stays in the same node, the value to go from one node to another is described in the corresponding ij position, and nodes there are not directly connected, an infinity sign is assigned.
In undirected graphs, the weight matrix is also symmetric. In directed not necessarily.


**DIJKSTRA'S ALGORITHM**: Used to find the shortest path between a starting node to all others in a weighted SIMPLE DIgraph (NO LOOPS OU PARALLELS). All weights must be positive. To apply the algorithm in an undirected graph you need to convert it in a digraph.
This metod finds the best path for each node separately, NOT the best way through many vertices.



##__KÖNIGSBERG BRIDGE PROBLEM__##

**WALK (or Path)**: A finite sequence of vertices in which each vertex is connected to the next by an edge in the graph. Can be declared only by writing the sequence of nodes. Is permitted an edge or a node to be repeated or the same edge to be crossed. A single edge with two nodes is considered a walk.
The walk is CLOSED if it ends at the same start note
The walk is OPEN if it ends in a  different node

**DIRECTED GRAPH**: a walk in a Digraph where all edges point in the same direction.

**LENGTH OF THE WALK**: the total of edges in the walk.

**CONNECTED GRAPH**: for every two random nodes there is a walk within them. A graph with only one node and a loop is considered connected.

**STRONGLY CONNECTED**: a digraph where for every random two nodes there is a direct path (one edge or more) to all nodes end the way back.


**----KÖNIGSBERG BRIDGE PROBLEM** Create a closed walk with 7 edges and 4 nodes starting with NO REPETITION. Impossible because all nodes have odd degrees.

**EULERIAN GRAPH** = THE GRAPH THAT CONTAINS AN EULERIAN CIRCUIT: a connected graph where ALL NODES MUST HAVE AN EVEN DEGREE. If a graph IS Eulerian all isomorphic-derived graphs will be Eulerian too.
A Digraph is eulerian if all nodes have the same in and out-degree. 
A Digraph is eulerian if it is strongly connected AND for each node, it is true that the input degree is equal to the output degree.


**EULERIAN TRAIL (or Eulerian Path)**: NO REPETITION OF EDGES + ALL EDGES ARE VISITED. 
MAY CONTAIN LOOPS AND PARALLELS, SO IT IS "OK" TO REPEAT NODES... 
EXISTS IF AND ONLY IF THERE ARE NO OR EXACTLY TWO ODD NODES (two because they will be the start and end respectively). All this without "removing the pencil from the paper".

**EULERIAN CIRCUIT**: A CLOSED EURELIAN TRAIL. Can be represented by a graph called Eulerian graph.

**HIERHOZER'S ALGORITHM**: Use to find the Eulerian Circuit in an undirected graph. Prerequisites: A connected graph that has only nodes with even degrees. Also called the Onion skin algorithm. The constructed closed walk resembles nested onion skins (it is a recursive algorithm)
    1. Choose a node and construct from it a subcycle K that does not pass through any edge twice. 
    2. If K is an Eulerian cycle, then break off. Otherwise, continue to step 3. 
    3. Neglect all edges of K. 
    4. At the first vertex of K, let a second subcycle K2 arise which contains no edge of K and no edge of the original graph twice. 
    5. Insert the second circle K2 into K.
    6. Continue with step 2.

**HOW TO SOLVE THE POSTMAN PROBLEM**: First, we must determine whether the graph is Eulerian. If it is not, we must make it so, thereby allowing us to use Hierholzer’s algorithm.

**Which one of the following sets of procedures reveals the correct way to solve the postman problem?**
Determine whether the graph is Eulerian. Then, search for node pairs with odd degrees and find the shortest connecting path. Double the edges of the shortest path and, finally, apply Hierholzer’s algorithm to find the Eulerian circuit.


##__HAMILTONIAN GRAPH AND THE PROBLEM OF THE TRAVELING SALESMAN__##

**PATH GRAPH (or LINEAR GRAPH)**: Linear Graph with pairwise edger =nodes-1.
P1 one node, P2 two nodes ...Pn n nodes.

**CYCLE GRAPH (not circle graph)**: nodes and edges are connected in a closed chain. 
C1 one node, C2 two nodes ...Cn n nodes. All cycle graphs are regular of degree 2, planar, and Eulerian.
Because of this definition, it is necessary for a bipartite graph to have at least two nodes and no loops (but it can have multiple edges). All cycle graphs Cn with an even number of nodes are bipartite.

**STAR GRAPH**: Has a central node that is connected to all other nodes (all other nodes are degree 1). The total of nodes = edges+1.
S1 one node out the center, S2 two nodes out the center ...Sn n nodes out the center.

**WHEEL GRAPH**: has total nodes >= 4 and all nodes are adjacent to each other and have a "central node" in the draw.
W4 four nodes, W5 five nodes ...Wn n nodes.

**COMPLETE GRAPH**: undirected simple graph (no loops or parallels) where there is an edge connecting every node. each node has degree = n-1 considering n as the total of nodes. So all complete graphs are also a Regular graph of degree n-1, so obviously in case of n is even the degree is odd and the graph will NOT be Eulerian. The total Number of edges: n * (n‒1)/2.
K1 one node, K2 two nodes ...Kn n nodes.
Is true that every subgraph with n nodes is a subgraph of Kn.


**BIPARTITE GRAPH (or BIGRAPH)**: the nodes are divided into two disjointed non-empty sets and THE EDGES ARE PLACED ONLY BETWEEN those sets, not inside them (each edge has one end in one set and the other in the opposite set). All cycle graphs with an EVEN number of nodes are bipartite. Normally are called Km,n where m and n represent the number of nodes in each set and those numbers are separated by a comma. 
The stargraph is also a Bipartite graph where Sn = K1,n


**KURATOWSKI'S THEOREM**: Considering K5 and K3,3 as the smallest NON-PLANAR graph, the theorem says that a graph G is planar if and only if G does not contain a subgraph equal to K5 or K3,3.



**-----HAMILTONIAN GRAPH** the graph that contains a Hamiltonian Cycle.
**Hamiltonian Cycle**: CLOSED WALK THAT CONTAIN EACH NODE EXACTLY ONCE.
No repetition of nodes and no repetition of edges consequently. DO NOT NEED TO VISIT EVERY EDGE.
If is a digraph needs to respect the orientation (also called directed Hamiltonian cycle).
If a graph is isomorphic to a Hamiltonian that will be also Hamiltonian.

**HAMILTONIAN PATH (SEMI-HAMILTONIAN GRAPH)**: Hamiltonian OPEN walk/path. 

**Edge bridge**: if you remove that edge from a graph the graph becomes Disconnected.
**IF THERE IS A BRIDGE EDGE IN A GRAPH THIS GRAPH IS NOT HAMILTONIAN**.
 
///////////////////
**PATH GRAPHS**:  are NOT EULERIAN and NOT HAMILTONIAN
**CYCLE GRAPHS**: are EULERIAN and HAMILTONIAN
**STAR GRAPHS**:  are NOT EULERIAN and NOT HAMILTONIAN
**WHEEL GRAPHS**:  NOT EULERIAN but they are HAMILTONIAN
**COMPLETE GRAPHS**: (undirected simple graph each node has degree = n-1):  are EULERIAN for odd nodes, and are HAMILTONIAN for nodes >2
**SANTA'S HOUSE**:  NOT EULERIAN but is HAMILTONIAN
\\\\\\\\\\\\\\\\\\

**TO CALCULATE THE NUMBER OF POSSIBLE HAMILTONIAN CICLES IN A COMPLETE GRAPH**     Kn  ==>      (n-1)! / 2
In the case of simple graphs, this formula also applies but the result is ~at most~ the total Hamiltonian cycle possibilities.

**At this moment there is no efficient algorithm for deciding whether a graph is Hamiltonian and there is no efficient algorithm to find the Hamiltonian cycle in a graph (because this a a non-polinomial problem at this moment).**

**The Ore and Dirac condition**... are auxiliary conditions to decide whether a graph is Hamiltonian.
If both conditions are true then the graph IS Hamiltonian, but if not it does NOT mean that the graph is not Hamiltonian. Ex: the graph C5 is Hamiltonian BUT not satisfy the Ore condition.
**---Ore condition**: every graph with total nodes   >=3     the sum of the degree of all pairs of two non-adjacent nodes >= total nodes. 
**---Dirac condition**: the smallest degree of a node in the graph >= total nodes/2
If a graph satisfies the Dirac condition, then it also satisfies the Ore condition. However, if a graph satisfies the Ore condition, then it need not also satisfy the Dirac condition.


**Traveling salesman problem (or TSP)**. It differs from the Hamilton circle problem only in that the underlying graphs are weighted. The task is to find a round trip through all nodes that minimizes the sum of the distances traveled. So the task is to find a Hamiltonian cycle in a weighted graph such that the sum of the weights is minimal. Example: Electronic circuit board manufacturing. 
There is no exact algorithm that can solve the problem in an acceptable time. Of course, it is possible to determine all Hamiltonian cycles, compare the sum of the weights of each, and choose the cycle with the smallest weight. However, as described earlier, a simple graph with n nodes can have up to (n‒1)!/2 Hamiltonian cycles. There are a lot of possibilities to compare.
Therefore, some efficient approximation algorithms, called heuristics, have been developed in the last decades that can solve the traveling salesman problem with acceptable accuracy in an acceptable time, even with many nodes. However, a heuristic cannot guarantee that the optimal solution can actually be found. ***



##__TREES or TREE GRAPH__##

IS A CONNECTED GRAPH THAT DOES NOT CONTAIN ANY CLOSED WALK /DOES NOT CONTAIN ANY CYCLE. 
Many disconnected tree graphs = forest.
All star-graphs Sn are trees.
All path graphs (one-way line) Pn are also trees.
A tree DOES NOT have loops or parallels. If one random edge is removed then the tree falls in two, is not it originally was not a tree.
There is exactly one path between any two nodes, and the reverse is also true, so, if there is exactly one path between any two nodes of a graph without loops this graph is a tree.
* A connected graph is a tree IF and only if all edges are bridges (if you remove it the graph becomes disconnected).
*IS TRUE THAT IF A NODE CONTAINS A NODE WITH K DEGREE, THIS TREE WILL ALSO CONTAIN AT LEAST K LEAVES.

**LEAF (LEAVES)**: Node with degree 1, here it is about the degree, not the arrangement or interpretation. It is a node with no child. LEAVES HAS NO SUCESSOR.

**INTERNAL NODE**: A node with at least one child. If the root node has children then it is also an internal node.

**TOTAL EDGES OF A TREE** = total nodes-1.

**ROOTED TREE**: This is a tree where One node is designated as the root. A non-empty rooted tree contains exactly one root. Used to visualize hierarchical structures. The Root has NO predecessor. Considering the root is on top, you can CHILDREN the nodes below to an upper node and call the parent the node on top of the other node. Nodes with the same parents are brothers or siblings. A rooted tree with only one node and no child this solitary node is at the same time root and leaf.

**OUTDEGREE OF A TREE**: the maximum number of children of each node. Ex: a List tree has a maximum of 1 child per node.
**FULL TREE**: every node has the maximum number of children permitted by the outdegree, but not necessarily the final level of leaves will be complete
**COMPLETE TREE**: Full tree inclusive in the leaf level.

**HEIGHT OF A ROOT TREE**: the maximum depth (counted from 0 = the root is index 0) of a node (the length of the path)

**FREE TREE**: A tree without a specific root, any node could be the root.


###__BINARY TREE___###
IS a rooted tree with outdegree =2. The children are called the left and right child.

**THE TOTAL OF NODES IN A COMPLETE  BINARY TREE = (2ĥ+1)-1**     where h is the height, remember the root is height 0. 

The three main sequences to traverse binary trees --> systematic walk with a recursive algorithm to "visit" all nodes:

             A
        B        C
      D   E    F
    G

*****PRÉ-ORDER (node-left-right = NLR)**: First you visit a node, after you visit its children first left then right.
PreOrder Algorithm (bin.tree.root p)
    While p!= null
    print (p)
    PréOrder.GO(p.left)
    PŕeOrder.GO(p.right)
//the example tree in this algorithm prints: A B D G E C F


*****POST-ORDER (left-right-node = LRN)**: First you visit all nodes to the left if possible, if not go to the right, in the end print, then repeat.
    Algorithm PostOrder(bin.tree.root p)
        While p!= null
            PostOrder.GO(p.left)
            PostOrder.GO(p.right)
            Print (p)
//This algorithm will print: G D E B F C A

*****IN-ORDER (left-node-right = LNR)**: You first visit the descendent's  os left, after printing the node, and after visiting the right descendent, and repeat.
    Algorithm SimOrder (bin.tree.root p)
      while p != null
          SimOrder.GO (p.left)
            If p.left =null
          print(p)
          SimOrder.GO (p.right)
//The result printed will be in ascending numerical order if it was a binary numerical tree organized. In this case will print: G D B E A F C


###__BINARY SEARCH TREE__###: 
Is a binary tree where each data (node) has a key to identify and allows the data to be found quickly.
---- LEFT descendent: smaller
---- RIGHT descendent: larger.
If print IN-ORDER the key is output in ascendin order.
If print POST-ORDER the key are outputs the values of both subtrees before the root.
If print PRÉ-ORDER the root key is output first, before the subtrees. 
IN A BINARY SEARCH TREE THE OPERATIONS OF SEARCH, INSERT, REMOVE, ETC CAN BE PERFORMED RECURSIVELY.


**SPANNING TREE**: IS A TREE CONTAINING ALL NODES OF A GRAPH. Is created by selecting a closed walk from a graph that is not a tree and then removing an edge from this walk. This principle is used in electricity systems for instance, because if a line(edge)fails the system still works.
--- EVERY CONNECTED GRAPH CONTAINS AT LEAST ONE SPANNING TREE.
--- YOU CAN CALCULATE THE MAXIMUM NUMBER OF COMBINATIONS OF SPANNING TREES OF A GRAPH Kn:   total=n^(n-2)
The name of this formula is Cayley's formula.




...
...
...
