# 介绍

[ibd2sql](https://github.com/ddcw/ibd2sql)是一个使用`python3`编写的**离线解析**MYSQL INNODB存储引擎的`ibd文件`的工具. 无第三方依赖包, **纯python3代码**. 使用**GPL-3.0** license.



# 特点

1. **方便**: 提取表DDL
2. **实用**: 可替换库(--schema)/表(--table)名, 可在sql语句中输出完整的字段(--complete)
3. **简单**: 纯python3代码编写, 无依赖包.
4. **支持众多数据类型**: 支持所有mysql数据类型
5. **支持复杂的表结构**: 分区表, 注释, 主键, 外键, 约束, 自增, 普通索引, 前缀索引, 主键前缀索引, 唯一索引, 复合索引, 默认值, 符号, 虚拟字段, INSTANT, 无主键等情况的表
6. **数据误删恢复**: 可以输出被标记为deleted的数据
7. **安全**: 离线解析ibd文件, 仅可读权限即可
8. **支持范围广**: 支持mysql 5.6 or 5.7 or 8.0 or 8.4



测试例子: [docs/ALLTEST.md](https://github.com/ddcw/ibd2sql/blob/main/docs/ALLTEST.md)



# 下载使用

本工具使用纯`python3`编写, 无依赖包, 所以建议直接使用源码.

V1.4 版本下载地址: <https://github.com/ddcw/ibd2sql/archive/refs/tags/v1.4.tar.gz>

## 下载

```shell
wget https://github.com/ddcw/ibd2sql/archive/refs/heads/main.zip
unzip main.zip
cd ibd2sql-main
```

## 使用

WIN/Linux用法完全一样

```shell
python3 main.py /data/mysql_3314/mysqldata/ibd2sql/ddcw_alltype_table.ibd --sql --ddl
```

更多使用方法或者5.7环境请看:  [docs/USAGE.md](https://github.com/ddcw/ibd2sql/blob/main/docs/USAGE.md)



# 版本更新

| 版本   | 更新时间       | 说明                |
| ---- | ---------- | ----------------- |
| v0.1 | 2023.4.27  | 第一个版本             |
| v0.2 | 2023.08.30 | 支持更多数据类型          |
| v0.3 | 2023.10.13 | 支持5.7升级到8.0的ibd文件 |
| v1.0 | 2024.01.05 | 支持debug,支持更多类型和功能 |
| v1.1 | 2024.04.12 | 修复一些bug           |
| v1.2 | 2024.04.25 | 新增空间坐标的支持         |
| v1.3 | 2024.05.11 | 支持mysql 5.6, 5.7  |
| v1.4 | 2024.05.21 | 支持溢出页, 子分区        |

详情: [docs/CHANGELOG.md](https://github.com/ddcw/ibd2sql/blob/main/docs/CHANGELOG.md)



# 要求和支持范围

要求: python3

支持范围: mysql5.x 8.x
