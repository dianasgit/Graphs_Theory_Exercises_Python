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


















