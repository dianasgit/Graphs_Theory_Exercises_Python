########################### MATRIX #############################

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
      If the determiannte = 0 than the matrix is NOT invertible.

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





    Grafo: Um grafo é uma coleção de vértices (ou nós) e arestas que conectam pares de vértices. Os grafos podem ser direcionados (arestas têm uma direção) ou não direcionados.

    Vértice: Um ponto em um grafo.

    Aresta: Uma linha que conecta dois vértices em um grafo.

    Grafo Direcionado: Um grafo no qual cada aresta tem uma direção, indicando a ordem dos vértices conectados.

    Grafo Não Direcionado: Um grafo no qual as arestas não têm direção específica.

    Passeio (ou Caminho): Uma sequência de vértices em que cada vértice é conectado ao próximo por uma aresta no grafo.

    Ciclo: Um passeio fechado em um grafo, onde o primeiro e o último vértices são iguais, e as arestas não são repetidas (exceto para a aresta que conecta o primeiro e o último vértices).

    Ciclo Euleriano: Um ciclo que passa por todas as arestas de um grafo exatamente uma vez. O grafo deve ser conectado.

    Grafo Conexo: Um grafo no qual existe pelo menos um caminho entre qualquer par de vértices.

    Grafo Desconexo: Um grafo que consiste em duas ou mais componentes conectadas, sem caminho entre essas componentes.

    Busca em Largura (BFS): Um algoritmo para percorrer ou pesquisar em grafos, onde você explora todos os vizinhos de um vértice antes de passar para os vizinhos dos vizinhos.

    Busca em Profundidade (DFS): Um algoritmo para percorrer ou pesquisar em grafos, onde você explora o máximo possível ao longo de cada ramo antes de retroceder.

    Árvore Geradora Mínima: Em um grafo ponderado, uma árvore geradora mínima é uma árvore que inclui todos os vértices do grafo, com o peso total das arestas sendo minimizado.

    Matriz de Adjacência: Uma matriz que representa as conexões entre vértices em um grafo. Na matriz de adjacência, os elementos indicam se existe ou não uma aresta entre os vértices.

    Matriz de Incidência: Uma matriz que representa as conexões entre vértices e arestas em um grafo.

    Grau de um Vértice: O número de arestas conectadas a um vértice.

    Grafo Bipartido: Um grafo cujos vértices podem ser divididos em dois conjuntos, de modo que todas as arestas conectam um vértice de um conjunto ao outro.

    Algoritmo de Dijkstra: Um algoritmo para encontrar os caminhos mais curtos entre um vértice de origem e todos os outros vértices em um grafo ponderado.
    Grafo Ponderado: Um grafo no qual cada aresta tem um peso associado que reflete alguma medida, como distância, custo, tempo, etc.

Ciclo Hamiltoniano: Um ciclo que visita cada vértice em um grafo exatamente uma vez, mas não necessariamente passa por todas as arestas.

Árvore de Abrangência (Spanning Tree): Uma subestrutura de um grafo que é uma árvore, conectando todos os vértices do grafo original.

Grafo Euleriano: Um grafo que contém um ciclo Euleriano. Cada vértice deve ter grau par.

Vizinhança de um Vértice: O conjunto de vértices adjacentes a um vértice específico.

Caminho Mínimo: O caminho com o menor peso entre dois vértices em um grafo ponderado.

Grafo Cíclico: Um grafo que contém pelo menos um ciclo.

Corte Mínimo: Um conjunto de arestas cuja remoção divide um grafo em dois componentes conectados.

Fluxo Máximo: O valor máximo de fluxo que pode passar de uma fonte para um destino em um grafo ponderado.

Teorema das Quatro Cores: Afirma que qualquer mapa plano pode ser colorido com no máximo quatro cores de modo que países adjacentes tenham cores diferentes.

Teorema das Árvores Geradoras Mínimas de Kruskal: Um método para encontrar uma árvore geradora mínima em um grafo ponderado.

Grafo Planar: Um grafo que pode ser desenhado em um plano sem que suas arestas se cruzem.

Sequência de Graus: Uma lista dos graus dos vértices de um grafo.

Grafo Regular: Um grafo no qual todos os vértices têm o mesmo grau.

Grafo Acíclico Direcionado (DAG): Um grafo direcionado que não contém ciclos.

Isomorfismo de Grafos: Dois grafos são isomorfos se existe uma correspondência biunívoca entre seus conjuntos de vértices e arestas que preserva as adjacências.

Percurso Euleriano: Um passeio que percorre cada aresta de um grafo exatamente uma vez.

Teoria dos Jogos em Grafos: Estuda estratégias e interações competitivas entre diferentes entidades em um grafo.

Grafo Intervalar: Um grafo que representa intervalos na linha real, onde vértices representam intervalos e arestas indicam sobreposições.

Grafo de Preferência: Usado para modelar relações de preferência entre diferentes objetos ou entidades.

Subgrafo: Um grafo formado por um subconjunto de vértices e arestas de um grafo maior.

    Teorema de Ore: Um teorema que estabelece uma condição suficiente para a existência de um ciclo Hamiltoniano em um grafo não direcionado.

    Grafo de Cayley: Um grafo associado a um grupo, onde os elementos do grupo correspondem aos vértices e as operações do grupo correspondem às arestas.

    Matroide: Uma estrutura matemática abstrata que generaliza propriedades fundamentais de árvores geradoras mínimas e conjuntos independentes em grafos.

    Grafo Perfeito: Um grafo no qual o número cromático de qualquer subgrafo é igual ao seu número máximo de cliques.

    Número Cromático: O menor número de cores necessárias para colorir os vértices de um grafo de modo que vértices adjacentes tenham cores diferentes.

    Grafo de Intervalo-Partição: Um grafo formado pela união de intervalos em uma linha real, onde a interseção ocorre apenas entre extremidades de intervalos.

    Grafo Hiperbólico: Um grafo usado para modelar redes complexas, como redes sociais, que exibem características hiperbólicas em sua estrutura.

    Grafo Esparsificador: Uma subestrutura de um grafo que retém características importantes enquanto reduz o número de arestas.

    Matriz Laplaciana: Uma matriz associada a um grafo, que é útil em várias aplicações, incluindo análise de circuitos elétricos e teoria dos campos de Markov.

    Grafo Geodésico: Um grafo onde cada aresta representa o caminho mais curto entre os vértices conectados.

    Matriz de Adjacência: Uma matriz quadrada AA de ordem n×nn×n (onde nn é o número de vértices no grafo) usada para representar grafos não ponderados. O elemento aijaij​ é 1 se há uma aresta entre os vértices ii e jj, e 0 caso contrário. Em grafos direcionados, a matriz pode não ser simétrica.

    Matriz de Incidência: Uma matriz BB de ordem n×mn×m (onde nn é o número de vértices e mm é o número de arestas) usada para representar grafos. Se a aresta jj incide no vértice ii, então bij=1bij​=1 se a aresta sai de ii, −1−1 se a aresta chega em ii, e 00 caso contrário.

    Matriz de Laplaciana: Uma matriz LL de ordem n×nn×n associada a um grafo não direcionado, definida como L=D−AL=D−A, onde DD é a matriz diagonal dos graus dos vértices e AA é a matriz de adjacência. A matriz Laplaciana tem propriedades únicas relacionadas à conectividade e ciclos no grafo.

    Caminhos em Matrizes de Adjacência: A potência de AA (AkAk) fornece informações sobre o número de caminhos de comprimento kk entre pares de vértices no grafo.

    Matriz de Distâncias: Uma matriz que contém as distâncias mais curtas entre todos os pares de vértices em um grafo ponderado. Pode ser calculada usando algoritmos como o algoritmo de Floyd-Warshall.

    Autovalores e Autovetores: Os autovalores e autovetores da matriz de adjacência ou da matriz Laplaciana estão relacionados a propriedades importantes do grafo, como conectividade e estrutura modular.

    Matriz de Incidência Orientada: Uma variação da matriz de incidência usada para grafos direcionados, onde as colunas representam as arestas e as linhas representam os vértices, com entradas indicando a orientação da aresta.

    Álgebra de Matrizes e Grafos: A álgebra de matrizes pode ser usada para realizar operações sobre grafos, como multiplicação de matrizes para computar a matriz de caminhos mais curtos ou encontrar o número de caminhos entre vértices.

    Matriz Esparsa: Devido à natureza muitas vezes esparsa de grafos reais, representar matrizes de adjacência e de incidência como matrizes esparsas pode economizar espaço de armazenamento.

    Teorema do Determinante da Árvore Geradora Mínima: O determinante de uma matriz obtida removendo qualquer linha e a coluna correspondente de uma matriz Laplaciana é igual ao número de árvores geradoras mínimas do grafo.
    



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






























