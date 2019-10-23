# Supplai Style Guide

## Padrões

Para arquivos ou pasta componentes, usar o padrão `PascalCase`.
Ex:

- ApartmentManager
- FinancialDashboard

## Definições

_Pages_  
A pasta relativa ao gerenciamento das pages, _/src/pages_, deverá conter uma estrutura hierárquica respeitando os prefixos das rotas do site. Sendo elas:

- Supplier: fornecedores
- ApartmentManager: síndico
- CondoAdmin: administradoras

## Rotas

_Estrutura de pasta das rotas_

- Suplier: fornecedores
- ApartmentManager: síndico
- CondoAdmin: administradoras

## Auth

- Actions de autentitação apenas nas `actions` do redux
- Salvar dados retornados da autenticação no `storage` e no `redux`.
- Os dados deverão ser usados somente os que estão no `redux`, não diretamente vindo do storage

## CSS-in-JS

- Utilizar `styled-component`
- Evitar outros tipos de componentização sem a necessidade
- Utilizar as `props` para particularidades de cada _component_
- Não escrever cores diretamente no código, registrar a cor diretamente em `global/colors`
- Não escrever tamanhos diretamente no código, registrar tamanhos diretamente em `global/metrics`

## Variáveis

- Evitar ao máximo uso de var
- Usar const para variáveis definidas apenas uma vez no escopo
- Usar let para variáveis que sofrem alterações na execução
- Usar padrão snake case para nomes de variáveis

## Controle de estados

- Evitar estados no próprio componente
- Evitar prop-driling, se um estado passa para mais de um componente hierarquicamente, colocar em estado global

## API

- Não colocar chamadas para _urls_ diretamente na action, apenas utilizar os endpoints pré-definidos em `services/api`
- Todas as chamadas à _API_ deverão ser feitas através de `actions` do `redux`
- Não trabalhar diretamente com os dados vindos da API, e sim dos dados que forem enviados para o _redux_.

## Persistência de Dados

- Salvar dados importantes no storage, utilizando o `rehydrate` do `redux-saga` para realimentar o `redux`
- Utilizar os dados diretamente do `redux`, não diretamente do `storage` (ver item anterior)

## Componentes

- Use `object component` para componentes que necessitem de ciclo de vida (componentDidMount, etc)
- Use `functional component` para componentes sem ciclo de vida mas com controle de estados
- Use `stateless component` para componentes sem ciclo de vida, sem controle de estados mas que tenha outros componentes em uso
- Use `styled component` para componentes focados em layout
- Se um componente for focado em layout e necessitar de variantes, procure utilizar via `props` no próprio `styled component`, não criar um outro componente apenas para trabalhar com _props_

## Coding style guide

- Usar sintaxe literal para definição de objetos. Ex: `let response = {};`
- Cuidado com palavras reservadas do sistema em objetos, tais como (class, private, int, catch)
- Usar sintaxe lietaral para definição de arrays. Ex: `let items = []`
- Para copiar itens de um objeto
- Utilize aspas simples para strings. Ex: `let name = 'Samuel'`
- Use `tabs` marcado como `2 espaços`
- Coloque espaço entre operadores como `let valor = 1 + 5;`
- Utilize `;` no final de cada linha que conclui um comando
- Escreva funções, variáveis e objetos com nomes auto-explicativos. Ex: `let valor_produto;` no lugar de `let vp;`
- Utilize `PascalCase` para `classes`
- Utilize `camelCase` para `funções`
- Utilize `snake_case` para `variáveis`
