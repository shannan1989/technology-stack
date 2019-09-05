# MySQL 字段在 DISTINCT、GROUP BY 时区分大小写

## 实现的方法有两种：

1. 使用 **binary** 属性修饰，如：

    ```sql
    CREATE TABLE `test` (
        `name` varchar(10) binary DEFAULT NULL,
        `sex` varchar(10) DEFAULT NULL
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
    ```

2. 正常创建表结构，在选择字符集（CHARACTER SET）时选择utf8mb4，选择排序规则（COLLATE）时选择**utf8mb4_bin**。

## 最终的表结构：

```sql
CREATE TABLE `test` (
    `name` varchar(10) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL,
    `sex` varchar(10) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```
