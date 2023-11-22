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
o grafo bipartido completo é aquele onde todos os elementos de U tme uma conecção com todos elementos de V. pode ser denotado como K3,5 (a virgula mostra que ele é bipartido)  por exemplo quando é um conjunto com 3 vertices e o outro com 4 e todas as ligaçõe possíveis entre ambos os sets foir feita.


GRAFO PLANAR = Aquele que pode ser desenhado 2D sem que haja cruzamento de suas arestas. Caso contrário é dito grafo Não-Planar.
Pode-se mudar os vertices de lugar, desde que não se mecha no grau. ex o grafo de um cubo 3d pode ser desenhado planar 2d.
todo grafo k1 ou k2 ou k3 ou k4 ou árvore É planar.

***** TEOREMA DA RELAÇÃO DE EULER = A quatidade de Facer de um grafo planar pode ser calculada como: faces = aresta - vertices + 2
lembrando que a área externa conta como face... e este é um teorema para grafo em sua forma planar.. se houver cruzamento de aresta ele não vale

































