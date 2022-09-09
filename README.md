# mysql-component-uuid_v4

Extending MySQL using the Component Infrastructure - Adding a UUID v4 generator user fonction.

```
 MySQL > install component "file://component_uuid_v4";
 Query OK, 0 rows affected (0.0005 sec)
 
 MySQL > select uuid_v4();
 +--------------------------------------+
 | uuid_v4()                            |
 +--------------------------------------+
 | 87cff962-d54e-40a2-8c74-86630990fa65 |
 +--------------------------------------+
 1 row in set (0.0002 sec)
```


