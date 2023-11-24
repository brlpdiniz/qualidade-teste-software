## 1 TESTE ESTRUTURAL (CAIXA BRANCA)
O teste estrutural baseia-se no conhecimento da estrutura interna do programa, sendo os 
aspectos de implementação fundamentais para a geração/seleção dos casos de teste a serem 
executados.

Obs: a maioria dos critérios da técnica estrutural utiliza uma representação de 
programa conhecida como “Grafo de Fluxo de Controle”

## 2 Os casos de teste no teste estrutural devem:
◉ Garantir que todos os caminhos independentes de um módulo tenham sido exercitados pelo menos uma vez;
◉ Exercitar todas as decisões lógicas em seus lados verdadeiro e falso;
◉ Executar todos os ciclos nos seus limites e dentro de seus intervalos operacionais;
◉ Avaliar as estruturas de dados internas

## 4 Grafo de Fluxo de Controle
O grafo de fluxo mostra o fluxo de controle
◉ Nós representam um ou mais processos
◉ Arestas representam o fluxo de controle
◉ Regiões do grafo são áreas limitadas pelas arestas e nós (incluindo a área fora do grafo)

## 5 represenstação do Grafo
◉ Grafo representa relações entre entidades  (o todo)
◉ Nós (ou vértices): representam as entidades  (bolas)            
◉ Arestas: representam as relações entre as entidades (linhas)          

◉ Nó de entrada (inicial): representa um ponto de entrada do programa ou sistema. Pode ter 1 ou mais nós de entrada.
◉ Nó de saída (terminal): um nó que não tem arcos saindo dele. Representa um ponto de saída de um programa ou sistema


## Os critérios estruturais são, em geral, classificados em:
◉ critérios baseados na complexidade,
◉ critérios baseados em fluxo de controle e 
◉ critérios baseados em fluxo de dados

## Como calcular quantidade de ared
◉ A quantidade de áreas do grafo  
◉ V(G) = P+1 onde P é a quantidade de nós predicado (são àqueles que podem desviar o fluxo da execução: if, while, switch, etc.) do grafo G

## Utilizam apenas características de controle da execução do programa, como comandos ou desvios, para determinar quais estruturas são necessárias Os critérios mais conhecidos são:
◉ Todos-Nós: exige que a execução do programa passe, ao menos uma vez, em cada vértice do grafo;
◉ Todas-Arestas: requer que cada aresta do grafo, isto é, cada desvio de fluxo de controle do programa, seja exercitada pelo menos uma vez;
◉ Todos-Caminhos: requer que todos os caminhos possíveis do programa sejam executados.

## Baseado em fluxo de dado
◉ Utilizam a análise de fluxo de dados como fonte de informação para derivar os requisitos de teste.
◉ Seleciona caminhos de teste de acordo com as definições e dos usos das variáveis do programa (potenciais usos)

## Caso de Teste
Para usar grafos para projetar casos de teste deve-se seguir os seguintes passos:
◉ Desenhar o grafo
◉ Calcular a complexidade ciclomática
◉ Determinar um conjunto base de 
caminhos independentes
## resumindo 
◉ Métodos estruturais se baseiam na estrutura de controle do programa
◉ Funções ou métodos mais simples podem ser testados com métodos funcionais (caixa preta) 
enquanto que funções ou métodos mais complexos podem ser melhor testados com 
métodos estruturais (caixa branca)

