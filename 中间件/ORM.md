# ORM

## 介绍

- Object-Relationl Mapping
- 作用是在关系型数据库和对象之间作一个映射，这样我们在具体的操作数据库的时候，就不需要去和复杂的 SQL 语句打交道

## 传统做法

- 建立数据库连接，获得 Connection 对象。
- 根据用户的输入组装查询 SQL 语句。
- 根据 SQL 语句建立 Statement 对象 或者 PreparedStatement 对象。
- 用 Connection 对象执行 SQL 语句，获得结果集 ResultSet 对象。
- 然后一条一条读取结果集 ResultSet 对象中的数据。
- 根据读取到的数据，按特定的业务逻辑进行计算。
- 根据计算得到的结果再组装更新 SQL 语句。
- 再使用 Connection 对象执行更新 SQL 语句，以更新数据库中的数据。
- 最后依次关闭各个 Statement 对象和 Connection 对象

### 缺点

- 流程复杂，且业务处理逻辑和数据存取逻辑完全混杂在一块
- 假如要对其中某些业务逻辑或者一些相关联的业务流程做修改，要改动的代码量将不可想象

## ORM 做法

- 提供对 Model，对数据操作完整的 API 封装，`实体模型`只需继承，调用具体的 API 即可
- 各类语言对 ORM 实现大体相同，可以自行了解下
