# select columns into tableName from tableName; 与 insert into tableName select columns from tableName; 区别：

select into from 目标表格不存在
inert into select from 插入已存在的表格中；

# sql 约束

## unique 约束唯一标识数据库表中 的每条记录；和 primary key 为列或者列集合提供唯一性保证；

## 每一个表可以有多个 unique ，但是只能有一个 primarykey；

# primary key

## 必须包含唯一值

## 不能包含 null

## 每个表只能有且只有一个 primary key;

# SQL 约束 alert 操作

## primary key

```sql
alert table tableName
drop primary key;

alert table tableName
add primary key(column[s];
```

```sql
alert table tableName
add foreign key (columnName)
references tableName(columnName);

alert table tableName
drop foreign key(columnName)；
```

# check

```sql
alert table tableName
add check  (exp);

alert table tableName
drop constraint colums;
```

# default

```sql
alert table tableName
alert columnName set default value;

alert table tableName
alert columnName drop default;
```

# alert colunm 修改已有表中的列

```sql
ALTER TABLE table_name
ADD column_name datatype
```

# auto-incerment

# is null, is not null

不能用比较运算符判断 表格中的值是不是 null，只能用 is null 或 is not null;

# isnull()

# 通用数据类型

| 类型             | 描述                                         |
| ---------------- | -------------------------------------------- |
| character        | 字符， 字符串, 固定长度                      |
| varchar          | 字符串，字符， 可变长度                      |
| binary           | 二进制串                                     |
| boolean          | 布尔， true false                            |
| varbinary        | 二进制串， 可变长度                          |
| integer          | 整数                                         |
| smallint         | 整数，精度 5                                 |
| integer          | 整数，精度 10                                |
| bigint           | 整数， 精度 19                               |
| decimal(p, s)    | 精确数值， 精度 p， 小数点后 s 位            |
| numeric(p, s)    | 同上                                         |
| float(p)         | 近似数值，尾数精度 p                         |
| real             | 近似数值，尾数精度 7                         |
| float            | 近似数值，尾数精度 16                        |
| DOUBLE PRECISION | 近似数值，尾数精度 16                        |
| date             | 存储年，月，日值                             |
| time             | 存储 小时，分，秒值                          |
| timestamp        | 存储 年月日小时分秒值                        |
| interval         | 由一段数字组成，表示一段时间，取决于取件类型 |
| array            | 元素是固定长度的有序集合                     |
| multiset         | 元素是可变长度的无序集合                     |
| xml              | 存储 xml 数据                                |

# 函数

| 名字    | 描述     |
| ------- | -------- |
| round() | 四舍五入 |
