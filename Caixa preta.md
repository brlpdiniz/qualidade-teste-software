# Revisão - 2º Bimestre

## Caixa Preta (Entrada e Saída apenas)

### Objetivos / O que é
- É uma técnica de teste, busca descobrir:
    * funções incorretas ou ausentes
    * erros de interface, nas estruturas de dados, nos acessos a bancos de dados externos, desempenho, inicilização e término
- Busca garantir que os requisitos do sistema são plenamente atendidos pelo software desenvolvido (foco nos requisitos funcionais)
- Não é seu objetivo a verificação interna dos processamentos do software
- Seu objetivo é verificar se os resultados estão compatíveis com os dados incluídos no sistema
- De simples implementação, o profissional que aplicará precisa ter conhecimento dos requisitos, suas características e dos comportamentos esperados

### Desafios
- Ter um planejamento mais apurado e transparente
para que se possa saber quais cenários serão
testados;
- Trabalhar com o conceito de massa controlada
(garantir simulação dos cenários testados);
- Automação do processo.

### Decomposição de Requisito
- Nesse tipo de método, a qualidade do teste depende da
variedade de cenários que se possa criar com base nos
requisitos.
- Os requisitos podem ser recompostos em:
    * Cenário primário (cenário ideal)
    * Cenário alternativo (variações do cenário atual, mas gerando o mesmo resultado final)
    * Cenário de exceção (onde se trata problemas e
inconsistências)

Cenário Primário
    Cliente realiza pagamento em dinheiro
Cenários Alternativos
    Cliente realiza pagamento com cheque
    Cliente realiza pagamento com cartão de crédito
Cenários de Exceção
    Cliente realiza pagamento com cartão inválido
    Cliente realiza pagamento com cheque bloqueado

### Análise de Documentos
- Neste método analisam-se documentos que
detalham comportamentos e regras de negócios.
- Quando se utiliza UML, pode-se fazer uso do
diagrama de atividades e do diagrama de estado.
* Regras de negócios: "leis" internas que uma empresa segue para alcançar seus objetivos e manter um ambiente operacional coerente e controlado
- O diagrama de atividades revela todos os caminhos
alternativos (caminhos positivos) e as situações que
impossibilitam a finalização desse evento (cenários
negativos).Refinamento Caso de Teste

### Refinamento Caso de Teste
- No planejamento de testes, busca-se cobrir o maior número de situações possíveis com a menor quantidade de cenários.
    * Refinamento por Partição de Equivalência
        - Conhecido também como teste de equivalência;
        - Faz uso de grupos com características comuns e que devem ter processamento similares.
    * Refinamento por Valores-limite
        - Teste baseado em diretrizes;
        - Se escolhem casos de testes onde erros mais comuns podem ocorrer.
    * Refinamento por Probabilidade de Erro
        - Baseado na experiência do testador.

#### TESTE DE PARTIÇÃO DE EQUIVALÊNCIA
- Divide o domínio de entrada de dados em classes (grupos de valores), onde cada classe representa um possível erro a ser verificado.
| Entrada | Valores Permitidos | Classes | Casos de Teste |
| ------ | ------ | ------ | ------ |
| Idade | entre 18 e 120 | 18 a 120 | idade = 20 |
| Idade | entre 18 e 120 | < 18 | idade = 10 |
| Idade | entre 18 e 120 | > 120 | idade = 150 |
| ------ | ------ | ------ | ------ |
| Quantidade salários mín | entre 1 e 3 | 1 a 3 | renda = 2 |
| Quantidade salários mín | entre 1 e 3 | < 1 | renda = 0,5 |
| Quantidade salários mín | entre 1 e 3 | > 3 | renda = 5 |
- A probabilidade de erro de qualquer valor em uma classe é a mesma, não sendo necessário testar todos os valores.

#### TESTE DE VALOR LIMITE
- Aqui, os valores-limite são os casos de testes naturais de cada classe identificada.
- Complementar à partição por equivalência.
- No método de partição por equivalência, o foco está nas condições de entrada, enquanto que as condições de saída não eram exploradas.
- No método de análise de valores-limite, tanto os valores de entrada quanto os de saída deverão ser analisados.

#### TESTE DE PROBABILIDADE DE ERRO
- Está baseado na intuição e experiência de testar condições que normalmente provocam erros.
- Erros tradicionais:
    * Tabelas Vazias ou Nulas
    * Nenhuma Ocorrência - Ex: processar pedidos pendentes mas não há nada pendente
    * Primeira Execução - Ex: primeira movimentação da conta, não havendo saldo anterior
    * Valores Brancos ou Nulos
    * Valores Inválidos e Negativos
