# Desafio: Processando e Transformando Dados pelo MySQL e Power BI.

## Introdução
Nesse desafio foi feita a criação de uma instância na Azure para MySQL, foi criado um Banco de dados com base disponível no github.
Foi feita a integração do Power BI com MySQL no Azure, e para finaliza foi verificado problemas na base a fim de realizar a transformação dos dados.

### 1. Configuração do Banco de Dados.
Na primeira imagem é feita a configuração do banco de dados MySQL na Azure:

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/98dc199b-7971-488e-87ba-ace690b0fffe)

### 2. Inserindo condigós MySQL.
Exemplo da inserção de códigos no shell da Azure, onde é feita a criação das tabelas. O código pode ser encontra na pasta do GitHub desse mesmo repositório.
Na imagem e mostrado os nomes das tabelas, coju o nome da Base de Dados e "azure_company".

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/173b58ea-1587-41c0-8c1b-22af1f347fbe)

### 3. Integração do Power BI com a Azure.
Nesse próximo passo é feita a integração do Power BI com o Banco de Dados MySQL da Instância na Azure.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/7da092ac-701d-4780-860f-cc9d00759f59)

### 4. Verificando os cabeçalhos e tipos de dados.
Renomeando as colunas e fazendo a exclusão das colunas que não serão ulteis para a análise de dados.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/61e61d9d-1e6b-4235-98bc-1792e216faa6)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/21b0a8a0-1658-4bb9-93eb-4657d76c730d)

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/7e3233a5-97b2-4279-a0f3-6f937d3659f7)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/3b4c0384-9c81-4c41-bbd1-2d21c7d3d3a7)

### 5. Modificando os valores das colunas para o tipo double preciso.
Na imagem e mostrada as modificações e transformação das outras tabelas.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/c1ffd47b-e59c-4128-b65c-d59351894764)

Transformação da Tabela Dependentes, antes e depois.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/e45517ce-b3a6-4432-a091-c0207ed1e7c3)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/5b8868fb-a35a-49cd-bf69-a8954b5cac4a)

Transformação da Tabela Dep_localização, antes e depois.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/2d549bf9-b5a2-47f3-9b15-dd698053f6e9)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/7421bed5-0802-4579-a3cd-64f753100295)

### 6. Verificando a existência dos nulos e analise a remoção.
Foi verificado a existência de um nulo, mas esse não sera removido e sim substituido.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/f7c7c3db-db49-4a9b-9440-543aa1b2a12f)

Foi verificado que o Nulo em Colaboradores é um gerente que responde a ele mesmo.
Os super_ssn são ID dos respectivos gerentes. É percebido que se trata do gerente chefe, pois o salário é o mais alto.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/d9740a10-ae2f-48a8-8888-b76ec7849fcf)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/19530acc-a0c8-4efb-8c5a-df12ba55f101)

### 7. Verificando se há algum departamento sem gerente.
Foi verificado que todos os departamentos estão com seus respectivos gerentes, pode ser visto os IDs referente aos departamentos de cada gerente responsável.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/2f86c794-ce7b-46d2-aa66-9cf61fd7a314)

### 8. Verificando o número de horas dos projetos.
Os dados da coluna de Horas foi modificado para Inteiro e arredondado as horas, também é visto que existe um colaborador que não preencheu o Banco de horas.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/91f57c02-1f57-47c2-9722-6d2a9e7f4826)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/239d4d2b-ef75-42aa-bee4-be8c02bdccd1)

### 9. Foi mesclado employee e departament para criar uma tabela "Colaborador Departamento".
Essa tabela é referente ao nome dos departamentos associados aos colaboradores, ao ser mesclado, a tabela base foi a employee , pois é influenciado no tipo da junção.

Veja o passo para ser feita o Mesclar entre tabelas:
1. Primeiro escolher a tabela base, que será a employee, depois aperta em "Combinar".
2. Logo em seguida escolher a opção "Mesclar consultas" e depois "Mesclar consulta como novas", tem que ser escolhida está opção, pois será criada uma nova tabela. Se essa opção não fosse escolhida, não seria criada uma nova tabela e sim seria sobre posto as informações na tabela existente.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/e11b311f-aca7-45cb-8f41-b00f836673b9)

Depois faça os proximos passos de acordo com a imagem:

3. Pode ser visto as setas apontando para as tabelas bases referente a criação do novos dados, onde pode ser visto a primeira tabela e a tabela segundaria.
4. Em seguida é necessário marcar os número de indentidade que serão as referências para a contrução da junção dos dados.
5. Depois é preciso marcar o tipo de junção. Depois que fizer todos os procedimentos aperte em "OK".

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/a120e1d1-b533-4bf2-9bc6-bb4b8c1ce45f)

Será criada a nova tabela, renomeei apertando em cima do nome da tabela. 

6. Os dados da tabela irão aparecer com um coluna tendo varias tabelas referente a cada linha.
7. Vamos aperta e marcar o botão "Expandir", para ser mostrados as novas informação dos dados na nova tabela.
8. Apos isso, será mostrada as novas colunas que estão nomeadas referente aos nomes de sua tabela mãe. Você irá renomear de acordo com um nome mais intuitivo, e escluir as colunas que não serão nescessárias.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/99b0ffb2-f5b4-427e-aec4-5384ed59b623)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/4a7a20f5-b697-4c58-9c42-421910fb8500)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/57f88d4e-9999-419d-9441-0d0c3ca2dc1e)

## 10. Mesclagem de colunas.
É feita a Mesclagem das colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores.

1. Primeiro você marca todas as colunas que irá usar.
2. Depois vá em "Mesclar Colunas" que está na aba "Transformar".
3. Ao clicar ira aparecer as opções, "Separador" e "Nome da Coluna". em separador você deixa "Espaço", e em nome da coluna você coloca o nome referente a ela. Depois aperte em "OK" e veja o resultado.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/62731de2-b7c2-4e49-8eb6-186e20fae8ae)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/b192eaa6-0629-44be-817d-0a30370d24c8)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/42f3009d-cd6b-4ab9-b177-b52148db03be)

## 11. Separando colunas complexas
Nessa etapa vamos criar outras colunas baseadas em um dado de uma unica coluna, que é conhecida como complexa, ou seja, é uma uma coluna que tem muitas informações e vamos dividir essas em formações criando outras colunas.

1. Primeiro marque a coluna escolhida.
2. Depois vá na aba "Transformar", aperte na opção "Dividir Coluna", depois em "Por Delimitador".
3. Deixe iqual está na imagem, normalmente o sistema ja identifica o demilitador, escolha a opção de 4 colunas e aperte em "OK".
4. Renomeei as novas colunas e exclua a que não for util.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/696664f7-de1e-4a61-a801-49a252d57a61)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/1e0af015-10b9-4660-8491-38838c633d7a)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/043bd45b-8986-41f8-998c-ef40f7bfca55)

## 12. Mesclando as tabelas de departamentos e localização.
Isso fará que cada combinação departamento-local seja único. 

1. O primeiro passo é você ir em "Combinar" e depois Mesclar nova coluna, como já foi encinado nos passos anteriores.
2. Depois você marque os IDs de acodo com a imagem para eles serem as bases onde iram puxar od dados.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/95b3dc1f-82c8-4cf9-9d22-49c179c56ab4)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/f93a1b6c-47c9-4278-864a-c1fe50954966)

3. Em seguida será criada a nova tabela, renomeei e também renomeei as colunas.
4. Depois faça a junção das colunas, para ficar departamento referente a sua localidade.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/1779609b-163b-4556-acc2-3471836ffa7b)

## 13. Realizando a junção dos colaboradores e respectivos nomes dos gerentes .
Essa junção é um poico mais complexa, para fazer isso vamos precisar mesclagem 2x de tabelas para chegar ao resultado escolhido. 

1. Primeiro vamos Combinar as Tabelas "departamente" e a nova Tabela "Colaborador Departamento".
2. Depois renomeei a nova tabela para "Gerente" e também renomeei a coluna para "Gerente" referente aos gerentes da coluna.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/8ffc65af-e299-4aa9-a46b-e10458734a46)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/e9ccbe1f-82c4-455f-bc6b-eac061ae9cd5)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/c920c389-f672-4eed-a010-e03b75b8e0d8)

3. Em seguida você irá combinar as novas tabelas, "Gerente" que é a base, com a tabela "Colaborador Departamento".
4. Atenção nesse proximo passo, pois você não irá mesclar uma nova tabela, é sim sobrepor a tabela "Gerente", pois se você criar uma nova, depois não irá conseguir exlui-lá.
5. Siga os passos referente as imagens e conclua a criação a atualização da tabela gerente.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/2a9b275f-e1e9-4c3e-a3da-e85b935fbc4d)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/5aff31a5-54c0-4fd2-9b8e-7e1d9f3f87c9)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/b39ac42c-a13b-4e80-8422-0158eb1895cf)

Pronto agora você consegue referenciar cada colaborador ao seu respectivo gerente.

## 14. Por que, o caso supracitado, podemos apenas utilizar o mesclar e não o atribuir. 
Irei explica por que usamos a opção mesclar e não atribuir. A diferença fundamental entre essas duas operações está relacionada ao tipo de transformação que você deseja realizar e ao resultado que espera obter em seus dados.

**Mesclar:** A operação de mesclagem é usada principalmente para combinar dados de duas ou mais tabelas com base em uma coluna ou conjunto de colunas em comum. 
Isso é útil quando você deseja agregar informações de diferentes tabelas para criar uma única tabela que contenha informações combinadas. 
Você pode usar mesclagens internas, externas ou outras variações, dependendo de como deseja que os dados sejam combinados.

**Atribuir:** A operação de atribuição é usada para simplesmente adicionar linhas de uma tabela a outra, criando uma tabela maior com os mesmos campos. 
Isso é útil quando você tem tabelas semelhantes com os mesmos campos e deseja empilhá-las verticalmente para criar uma única tabela maior.

Ou seja, a diferença é que em **Mesclar**, você irá juntar duas tabelas e criar novas colunas. Em **Atribuir**, você irá juntar tabelas e criar novas linhas.

## 15. Agrupando os dados a fim de saber quantos colaboradores existem por gerente.
Segue o exemplo:

1. Clic com o botão direito do mouse em cima da coluna que quer agrupar.
2. Depois vá na opção "Agrupar".
3. Aperte em "Avançado", escolha a coluna base que é "Gerente" e aperte em "OK".
4. Pronto, já pode ser visto o número de colaboradores que cada gerente é responsável.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/505ce1da-10cf-4582-b22f-9f5e5f5f835a)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/ece7867b-20de-484a-8878-36e8bc917b32)
![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/eca2b075-e13a-444f-a36e-7cc0a2781fe5)

## 16. Analise dos Dados.

E para finalizar foi feito um Dashboard simples para ter uma idéia da analise de onde os dados foram tratados.

![image](https://github.com/WenderesMiranda/processando-transformando-powerbi-mysql/assets/138307729/b336da78-ab6a-43af-b560-0d05f81daeee)


