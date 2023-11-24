# MATRIX #

TRANSPOSITION = is created by turning/swapping rows into columns and columns into rows.

mx1 = column vector.
1xn = row vector.

All matrix vector without the transposition sign ARE column vector... they will only be a row vector when it has the transposition sign.

DIAGONAL MATRIX = all elements outside the main diagonal are zero. The main diagonal can be ani number, even zero. The all zero matrix is a special type of diagonal matrix

TRIANGULAR MATRIX = is upper triangular if the upper of the main diagonal are numbers and the bottom is all zero, end lower triangular otherwise.

IDENTITY MATRIX = is a Diagonal matrix where all elements in the main diagonal are = 1. Is denoted by E.

SIMETRIC MATRIX = If you transpose a matrix and it maintains the same ->  A = At. The matrix must be square!
Every square diagonal and all square Identy are symmetric.

SKEW-SIMETRIC =  A = -At

ADITION OF MATRIX = just add elements of the same position.

IN ADDITION THOSE LAWS APPLIE:
*COMMUTATIVE: A+B= B+A
*ASSOCIATIVE: A+(B+C) = (A+B)+C
*ZERO MATRIX IS THE NEUTRAL ELEMENT IN ADITION: A+0 = O+A = A


SCALAR MULTIPLICATION = it just multiply each element of the matrix by a scalar (any real number different then zero). The following laws applied:
*COMMUTATIVE: x*A = A*x
*ASSOCIATIVE: (x*y)*A = x* (y*A)
*DISTRIBUTIVE: (x+y)*A = x*A+ y*A
or     x*(A+B) = x*A + x*B    
The neutral scalar is the number 1. The scalar 0 will return a zero matrix.
    

DECOMPOSITION THEOREM: ANY Square matrix A can be represented by the sum of A = B+C where B is symetric and C is skew-symetric of A.
B= 0,5*(A+At)
C= 0,5*(A-At)

    
DOT PRODUCT OF VECTORS: If a row vector is multiplied by a column vector, and you multiplie each correspond index and add one to another you will find out an real number = Scalar. Only applies to vectors with the same index. IN THIS CASE, COMMUTATIVE LAW APPLIES. at*b = bt*a. DIstributive law too.


MULTIPLICATION OF MATRICES: The number of columns of the first must be the same as the number of lines of the second because the multiplication is YOU MULTIPLY EACH ELEMENT OF THE FIRST WITH THE SAME ELEMENT-COLUMN-INDEX OF THE SECOND AND SUM.
*DIagonal matrices (all zero except the main diagonal) play an important role in multiplication because depending on the order of the multiplication the main diagonal will alter the row or the columns of the matrix result.
*THE NEUTRAL ELEMENT IN MATRIX MULTIPLICATION IS THE IDENTITY MATRIX. A*E = E*A = A
*LAWS OF MULTIPLICATION:
- ASSOCIATIVE: (A*B)*C = A*(B*C)
- DISTRIBUTIVE: A*(B+C) = A*B + A*C
- IDENTITY:  A*E = A
- ZERO MATRIX = O --> A*0 = 0
- SCALAR MULTIPLICATION WITH AN IDENTITY MATRIX MULTIPLICATION:  x*A = (x*E)*A
- POWER MATRIX CAN BE SIMPLIFIED:    A^s+t = A^s*A^t
                                      A^s*t = (A^s)^t
*****ATENTION: commutative law generally NOT apply to multiplication of matrices because   A*B != B*A




***********LAWS OF TRANSPOSITION************
* (At)t = A
* (A+B)t = At + Bt
* (x*A)t = x*At
* (A*B)t = Bt * At
* Et = E


    ********************INVERSE/REGULAR MATRICES ***********************

    Every real number x other than zero has a inverse value (x^-1), and when the inverse is multiplied by x the result must be = 1.
  The inverse can be found as    1/x = x^-1
  An inverse matrix MAY exist only for square matrices. Not every square matrix has as inverse.
  The multiplication of a matrix by its inverse is equal to the identity:   A*A^-1 = A^-1*A = E
  IF THE INVERSE MATRIX EXISTS THE MATRIX IS CALLED INVERTIBLE OU REGULAR. If not if called non-invertible or singular.

    IF THE DETERMINANTE IS DIFFERENT THAN ZERO THE MATRIX IS INVERTIBLE, because it represent that the rows or columns of the matrix are linearly independent.
      If the determinant = 0 than the matrix is NOT invertible.

    1  2  3       1  2  3  | 1  2         the determinante is=   x-y
    4  5  6       4  5  6  | 4  5          1*5*9  + 2*6*7 + 3*4*8 = x
    7  8  9       7  8  9  | 7  8          3*5*7  + 1*6*8  + 2*4*9 = y

In 2x2 matrices to calculate the inverse (if the det != 0) just exchange the elementos on the main diagonal and reserse the sign (*-1) the elements of the second diagonal. And divide each element of the matrix by the determinant (divide because is the inverse of the determinant that matters 1/det and multiplay 1/det id the same as directly divide by the det.)
*An square diagonal matrix can be inverse if all elements of the main diagonal are !=0 and to invert you just need the invert each element of the main diagonal separately, i.e, just put each one in the form of 1/x. A triangular uper or lower is also invertible if the main diagonal has NO zero element (if it has a zero the determinant will be also zero)
***GENERAL LAWS:
- Inversion and trasposition are interchangeable: (At)^-1 = (A^-1)t
- IF A is simetric then A^-1 is also simmetric
- Shock-shoe rule:  (A*B)^-1 = B^-1*A^-1

**SIMETRICAL ENCRYPTION PROCEDURE = multiply a message by a matrix to encrypt and multiply the result by the inverse of the matrix key to decrypt. 
***

 ***********ORTHOGONAL MATRICES *************
        A square matrix is called oRTHOGONAL IF, AND ONLY IF A^-1 = At.. For a Orthogonal matrix A, At is also orthogonal... So ALSO APPLIES  A * At = A * A^-1 = E
  IF the matrix is SIMETRIC = A * A =E

        

# _____________INTRODUCTION TO GRAPHS___________ #

Graph: A graph is a collection of vertices (or nodes) and edges that connect pairs of vertices. Graphs can be directed (edges have a direction) or undirected.

EDGE: A line that connects vertices (nodes) in a graph;

UNDIRECTED Graph: A graph in which edges do not have a specific direction;  G = ( V , E) whit a set of finite nodes V={v1,v2,...vn} and set of edges E={e1,e2,...em}. V CAN NOT BE AN EMPTY SET, it need at least onde node. 

DIRECTED GRAPH: A graph in which each edge has a direction, indicating the order of connected vertices;

ISOLATED NODE= a node that is not connected to any other node by an edge.

ADJACENT NODES / NEIGHBORS: Nodes that are directly connected by the same edge. In a loop, the node is its own neighbor. 

INCIDENT EDGE: the edge that connect a node(s) in question. You say, edge E is incident to the node v1 and v2 ...

PARALLEL EDGE or MULTIPLE EDGER: Connect the same two nodes;

LOOP: the edge that connect a node to itself

** SIMPLE GRAPH: graph withOUT parallel edges (multiple edges) and withOUT Loops.

FINITE GRAPH: A graph with a finite number of nodes and edges.

INCIDENCE FUNCTION: The nodes or nod that is connected to an edge. Write it as:   e1 |-> {v2, v4)  ; e2|-> {v5}loop

DEGREE OF A NODE or VALENCE or NODE DEGREE: the total os edger that are incident to a node, or START in that node. Isolated nodes have degree 0. Loops count 2. 

REGULAR GRAPH = a graph where every node has the same degree.

*** HANDSHAKING LEMMA: Euler state that: In any FINITE AND UNDIRECTED AND SIMPLE graph the sum of all nodes degrees is twice the number of edges.
THAN THE SUM OF ALL NODES DEGREES MUST BE EVEN. AND in every finite, undirectec and simple graph must exist at leat two nodes with the same degree.
Exemple is impossible to draw a graph with 7 nodes whet all nodes has degree 3 .. because de sum will be 21, an odd number.
Is also impossible draw a graph with 4 nodes with the respective degrees (1 , 2 , 3 , 4) the sum is even, BUT is impossible because must exist at least two nodes with the same degree.

***ISOMORPHIC GRAPHS: Two graph are called isomorphic if it exists a bijective mapping in each node. They contain the same number of node, edges and degrees. BUT is necessary to make the mapping to guarantee the exact relation of connections, because a graph with the same number of nodes, and edges and degree could not be isomorphic.



Walk (or Path): A sequence of vertices in which each vertex is connected to the next by an edge in the graph.

Cycle: A closed walk in a graph where the first and last vertices are the same, and edges are not repeated (except for the edge connecting the first and last vertices).

Eulerian Cycle: A cycle that traverses all edges of a graph exactly once. The graph must be connected.

Connected Graph: A graph in which there is at least one path between any pair of vertices.

Disconnected Graph: A graph consisting of two or more connected components, with no path between these components.

Breadth-First Search (BFS): An algorithm for traversing or searching graphs, where you explore all neighbors of a vertex before moving on to the neighbors of neighbors.

Depth-First Search (DFS): An algorithm for traversing or searching graphs, where you explore as far as possible along each branch before backtracking.

Minimum Spanning Tree: In a weighted graph, a minimum spanning tree is a tree that includes all vertices of the graph, with the total weight of edges minimized.

Adjacency Matrix: A matrix representing connections between vertices in a graph. In the adjacency matrix, elements indicate whether there is an edge between vertices.

Incidence Matrix: A matrix representing connections between vertices and edges in a graph.

Vertex Degree: The number of edges connected to a vertex.

Bipartite Graph: A graph whose vertices can be divided into two sets, such that all edges connect a vertex from one set to the other.

Dijkstra's Algorithm: An algorithm for finding the shortest paths between a source vertex and all other vertices in a weighted graph.

Weighted Graph: A graph in which each edge has an associated weight reflecting some measure, such as distance, cost, time, etc.

Hamiltonian Cycle: A cycle that visits each vertex in a graph exactly once, but not necessarily all edges.

Spanning Tree: A substructure of a graph that is a tree, connecting all vertices of the original graph.

Eulerian Graph: A graph that contains an Eulerian cycle. Each vertex must have an even degree.

Vertex Neighborhood: The set of vertices adjacent to a specific vertex.

Shortest Path: The path with the smallest weight between two vertices in a weighted graph.

Cyclic Graph: A graph that contains at least one cycle.

Minimum Cut: A set of edges whose removal divides a graph into two connected components.

Maximum Flow: The maximum value of flow that can pass from a source to a destination in a weighted graph.

Four Color Theorem: States that any planar map can be colored with at most four colors such that adjacent countries have different colors.

Kruskal's Minimum Spanning Tree Theorem: A method for finding a minimum spanning tree in a weighted graph.

Planar Graph: A graph that can be drawn on a plane without its edges crossing.

Degree Sequence: A list of the degrees of the vertices in a graph.

Regular Graph: A graph in which all vertices have the same degree.

Directed Acyclic Graph (DAG): A directed graph that does not contain cycles.

Graph Isomorphism: Two graphs are isomorphic if there is a bijective correspondence between their sets of vertices and edges that preserves adjacencies.

Eulerian Path: A walk that traverses each edge of a graph exactly once.

Game Theory in Graphs: Studies strategies and competitive interactions between different entities in a graph.

Interval Graph: A graph representing intervals on the real line, where vertices represent intervals and edges indicate overlaps.

Preference Graph: Used to model preference relations between different objects or entities.

Subgraph: A graph formed by a subset of vertices and edges from a larger graph.

Ore's Theorem: A theorem that establishes a sufficient condition for the existence of a Hamiltonian cycle in an undirected graph.

Cayley Graph: A graph associated with a group, where group elements correspond to vertices and group operations correspond to edges.

Matroid: An abstract mathematical structure that generalizes fundamental properties of minimum spanning trees and independent sets in graphs.

Perfect Graph: A graph in which the chromatic number of any subgraph is equal to its maximum clique number.

Chromatic Number: The smallest number of colors needed to color the vertices of a graph such that adjacent vertices have different colors.

Interval-Partition Graph: A graph formed by the union of intervals on a real line, where intersection occurs only between interval endpoints.

Hyperbolic Graph: A graph used to model complex networks, such as social networks, exhibiting hyperbolic characteristics in their structure.

Sparse Graph: Due to the often sparse nature of real-world graphs, representing adjacency and incidence matrices as sparse matrices can save storage space.

Maximum Flow Theorem: The value of the determinant of a matrix obtained by removing any row and the corresponding column of a Laplacian matrix is equal to the number of minimum spanning trees in the graph.

    





########### GRAFO EULERIANO #############

* Teoremas auxiliares para resolução:
- 1 - Seja S a soma dos graus de todos os vértices de um grafo G, temos que S é o dobro da quantidades de arestas deste grafo, portando S é par.
- 2 - Todo grafo G possui um número par de vértices de grau ímpar (ou nenhum), é impossível haver uma quantidade impar de vértices com grau ímpar, pois se não quebra o teorema 1.


UM GRAFO SERÁ EULERIANO QUANDO EXISTE UMA TRILHA FECHADA (não repete arestas / começa e termina no mesmo vértice) QUE PASSA POR TODAS AS ARESTAS DE G.

UM GRAFO SERÁ SEMI-EULERIANO É QUANDO EXISTE UMA TRILHA QUE PASSA POR TODAS AS ARESTAS SEM REPETIR TAMBÉM, MAS ELE COMEÇA E TERMINA EM VÉRTICES DIFERENTES.

****TEOREMA DE EULER (1736): Um grafo conexo G é Euleriano se, e somente se, todos seus vértices tem grau par.

* Teorema semi-euleriano: Um grafo conexo G é semieuleriano se, e somente se, G tem dois vértices de grau ímpar. Para este dar certo você deve iniciar em uma aresta de grau impar e terminar na outra aresta de grau ímpar.

No grafo em que o número de arestas com grau ímpar for maior que 2 é impossível passar por todas as arestas sem repetição, portanto ele NÃO É EULERIANO NEM SEMIEULERIANO.


===================== GRAFO HAMILTONIANO =========

CICLO HAMILTONIANO = UM CICLO (não repete arestas , não repete vértice exceto  a primeira pois é a mesma onde termina) que passa por todos os vértices de um grafo G.
GRAFO HAMILTONIANO = Um grafo será hamiltoniano quando pode existir um ciclo hamiltonia nele.

O PROBLEMA É QUE O GRAFO HAMILTONIANO É NÃO POLINOMIAL-COMPLETO

ESTA TEORIA ILUSTRA O PROBLEMA DO CAIXEIRO VIAJANTE. ELE PREVISA PASSAR POR TODAS AS CASAS (ARESTAS) SEM REPETI-LAS, MAS NÃO NECESSARIAMENTE PRECISA PASSAR TODAS AS RUAS.


///////////////// GRAFO VALORADO / PONDERADO \\\\\\\\\\\\\\\\\\\\\\\\\

É o grafo que possui um peso, valor atribuído para cada aresta, esse valor pode indicar distâncias, tempos, custos, etc.

pode-se criar uma MATRIZ DE DISTÂNCIAS onde cada valor Gij é preenchido com a distancia entre os vértices, e assim como toda matriz de gráfo se o grafo não for direcionado a matriz será simética em relação à diagonal principal, e se não houver loops a diagonal principal é toda zero. Quando não há ligação doreta entre as arespas pode-se preencher com zero também.



========== ALGORITMO DE DIJKSTRA =================
É o algoritmo que determina o caminho "mais curto/com menor custo" num grafo com arestas de peso não negativo em tempo polinomial.







$$$$$$$$$$$$$$$$ PROBLEMA DO CAIXEIRO VIAJANTE $$$$$$$$$$$$$$$
Dado um grafo valorado G, desejamos determinar o valor do menor ciclo hamiltoniano, ou seja, passa por todos os vertives sem repetir aresta e o único vértice que se repete é o inical pois termina-se neste, todos os outros não pode repetir também. Ou seja, deve-se visitar todos os vertices sem repetir, aresta nem vertice e terminar no mesmo ponto que se iniciou e percorrer a menor distancia/valor possível.






========================GRAFO PLANAR ===========================

GRAFO BIPARTIDO (BIGAFO)= é o grafo cujo os vértices podem ser divididos em dois conjuntos distindos U e V tais que TODA ARESTA conecta um vértice U a um vertice V. U e V são sets sem conecção interna entre si.
o grafo bipartido completo é aquele onde todos os elementos de U tem uma conecção com todos elementos de V. pode ser denotado como K3,5 (a virgula mostra que ele é bipartido)  por exemplo quando é um conjunto com 3 vertices e o outro com 4 e todas as ligaçõe possíveis entre ambos os sets foir feita.


GRAFO PLANAR = Aquele que pode ser desenhado 2D sem que haja cruzamento de suas arestas. Caso contrário é dito grafo Não-Planar.
Pode-se mudar os vertices de lugar, desde que não se mecha no grau. ex o grafo de um cubo 3d pode ser desenhado planar 2d.
todo grafo k2 ou k3 ou k4 ou toda árvore É planar.

***** TEOREMA DA RELAÇÃO DE EULER = A quatidade de Faces de um grafo planar pode ser calculada como: faces = aresta - vertices + 2
f=a-v+2
lembrando que a área externa conta como face... e este é um teorema para grafo em sua forma planar.. se houver cruzamento de aresta ele não vale

****1º TEOREMA PARA DESCOBRIR SE É PLANAR = se o grafo G é planar então é valida a seguinte relação:
a<= 3*v-6
SE der = é porque G é MAXIMAL PLANAR, ou seja, se add uma nova aresta fica impossível ele ser planar.
Se der falso então com certeza Não é planar... porém há grafos não planares que conseguem o resultado verdadeiro neste teorema, portando existe a segunda parte:

*** 2º TEOREMA PARA DESCOBRIR SE É PLANAR = TEOREMA DA CONTRAPOSIÇÃO.
Lembrando da logica de contraposição que (a=>b) <=> (!b => !a) 
portanto se aplicar a negação da formula do teorema 1 o resultado precisa ser a negação do resultado, portante negar a formula gera resultado Não planar.

se     a>3*v-6 então o grafo não é planar.
Então quando o grafo passar pelo primeiro teorema como positivo para planar, faça a contraprova para ter certeza.
Porém atenção que grafos bipartidos enganam esses dois teoremas e geram resultados errados, desta forma deve-se usar o teorema 3.

***** 3º TEOREMA PARA BIPARTIDOS PLANARES = Se um grafo bipartido É planar a seguinte relação é valida:    a<= 2*v-4

A contraposição deste teorema também vale como prova então
se a>2*v-4 for verdade então o grafo NÃO é planar bipartido.
por ex o grafo K3,3 da brincadeira de criança de ligar 3 casas à linha de telefone, luz e água sem cruzar as linhas é comprovadamente imposssível pelo teorema 3 da contraposição






























