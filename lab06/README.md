# Equipe `VASKO`

# Subgrupo `VASCO`
* Gabriel de Carvalho Silva Nascimento - 222103
* Breno Shigeki Guimarães Nishimoto - 220599
* Mateus da Costa e Silva Rios Alves de Andrade - 230806

## Tarefa de Cypher sobre Patologias, Medicamentos e Efeitos Colaterais

## Exercício

Faça a projeção em relação a Patologia, ou seja, conecte patologias que são tratadas pela mesma droga.

### Resolução
~~~cypher
MATCH (p1:Pathology)<-[a]-(d:Drug)-[b]->(p2:Pathology)  
WHERE a.weight > 20 AND b.weight > 20  
MERGE (p1)<-[s:Similar]->(p2)  
ON CREATE SET s.weight=1  
ON MATCH SET s.weight=s.weight+1
~~~

# Trabalhando com Efeitos Colaterais

## Exercício

Construa um grafo ligando os medicamentos aos efeitos colaterais (com pesos associados) a partir dos registros das pessoas, ou seja, se uma pessoa usa um medicamento e ela teve um efeito colateral, o medicamento deve ser ligado ao efeito colateral.

### Resolução
~~~cypher
#Carrega as pessoas:
LOAD CSV WITH HEADERS FROM 'https://raw.githubusercontent.com/santanche/lab2learn/master/data/faers-2017/drug-use.csv' AS line  
CREATE (:Person {idperson: line.idperson})

#Cria relações pessoa->droga:
LOAD CSV WITH HEADERS FROM 'https://raw.githubusercontent.com/santanche/lab2learn/master/data/faers-2017/drug-use.csv' AS line  
MATCH (d:Drug {code: line.codedrug})  
MATCH (p:Person {idperson: line.idperson})  
CREATE (p)-[:Takes {pathology : line.codepathology}]->(d)

#Para cada linha, cria uma aresta de todas as drogas daquela pessoa para essa patologia:
LOAD CSV WITH HEADERS FROM 'https://raw.githubusercontent.com/santanche/lab2learn/master/data/faers-2017/sideeffect.csv' AS line  
MATCH (p:Person {idperson: line.idPerson})-[:Takes]->(d)  
MATCH (pa:Pathology {code: line.codePathology})  
MERGE (d)-[i:Induces]->(pa)  
ON CREATE SET i.weight=1  
ON MATCH SET i.weight=i.weight+1
~~~

## Exercício

Que tipo de análise interessante pode ser feita com esse grafo?

Proponha um tipo de análise e escreva uma sentença em Cypher que realize a análise.

### Resolução
Resolvemos tentar identificar remédio que induzem com maior frequencia do que tratam certas doenças, com um mínimo de 20 tentativas de tratamentos, para evitar coincidencias e outliers
~~~
MATCH (d:Drug)-[a:Induces]->(p:Pathology)<-[b:Treats]-(d:Drug)  
WHERE a.weight > b.weight AND b.weight > 20  
RETURN d, p  
LIMIT 50
~~~