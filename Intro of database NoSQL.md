# Introdução ao Banco de Dados NoSQL - Não relacional

### O que é um banco de dados não relacional?

Um banco de dados mais fléxivel e dinâmico, armazenam tipos mais fléxiveis tais como: JSON (JavaScript Object Notation), chave-valor, colunas ampla ou grafos.

`Detalhe: SQL é APENAS uma linguagem de consulta || NOSQL é uma abordagem de gerenciamento de bancos de dados.`

### Quais as vantagens?

Fléxivel, dinamico e escalabilidade. NoSQL surgiu numa necessidade da tecnologia, onde era necessário uma melhor escalabilidade vertical (CPU e RAM) já que adição de mais CPU e RAM rapidamente pegava um teto muito rapido, e escalabilidade horizontal, já que é possivel fragmentar os arquivos e separa-los eles em discos diferentes,ou seja, permitindo ter um cluster de banco de dados, ou seja nós, maquinas juntas que se somam em um banco de dados, embora seja bem complexo.

### Por que escolher um banco de dados NoSQL

Quando exige uma necessidade de uma escalabilidade e flexibilidade do banco de dados, o banco de dados NoSQL surge como uma solução arquitetural, onde o mesmo permite uma maior flexibilidade de armazenamento e de consulta SQL. 

### Resumo histórico

- Surgimento no final dos anos 2000.
- Surgimento do Google Bigtable, um banco de dados de colunas largas, mas publicado em 2015, uma parte do Google Cloud
- Introdução do primeiro banco de dados orientados a documentos, MongoDB em 2009
- Surge novos Bancos de Dados NoSQL, Apach HBase (Wide-column || Colunas amplas), Cassandra (wide column), CouchBase (Key-value cache) e Neo4j(Grafo) em 2010
- Amazon intruduz DynamoDB (chave valor) em 2012
- MongoDB Atlas, um DBSaaS em 2016 surge.
- Azure CosmosDB (Banco de dados chave-valor)

### Comandos MongoDB

#### Inserir documento dentro da coleção
```javascript
db.NomeDaCollection.insertOne({
    id: objectId(), // Se for deixar a seleção de id automatica não precisa escrever essa parte
    title: "Teste", // Obrigatório a descrição ser entre aspas ou aspas dupla
    description: "Foi realizado teste", // Assim como linguagem de programação, em caso de escrever outro parâmetro necessário a utilização da virgula.
})
```

`Observação o comando .insert() se tornou obsoleto, e não se utiliza mais. Ficando então .insertOne() ou .insertMany()`

#### Ver os itens dentro da minha coleção estruturado

```javascript
    db.NomeDaCollection.find().pretty() // Retorna todos os documentos dentro da minha coleção, o .pretty() é comumente usado para retornar os valores estruturados, já que o .find() sozinho não retorna com estruturação
```

#### Deletar um documento dentro da minha coleção

```javascript
    db.NomeDaCollection.deletOne(
        {_id: ObjectId('68aec48653f38ce149a75ac7'}
    );
```