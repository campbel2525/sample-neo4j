# Neo4j とは

Neo4j はグラフデータベースの一つで、データを「ノード」と「リレーションシップ」で表現します。

## 主な特徴

- ノード(エンティティ)とリレーションシップ(関係)でデータを保持する
- クエリ言語は Cypher を使用する
- 関係の走査が高速で、SNS や推薦、経路探索などに向いている

## Cypher の例

```cypher
CREATE (a:Person {name: 'Alice'})-[:KNOWS]->(b:Person {name: 'Bob'})
RETURN a, b
```

```cypher
MATCH (p:Person)-[:KNOWS]->(friend)
RETURN p.name, friend.name
```
