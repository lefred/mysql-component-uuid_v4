# mysql-component-uuid_v4

Extending MySQL using the Component Infrastructure - Adding a UUID v4 generator user function.

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

# Compilation notes

Since MySQL 8.3.0, boost is included in the source code (extra directory), but it's not a full
version, some modules are missing to compile this component.

You need to copy them first:

```
cp -r boost_1_77_0/boost/uuid/ mysql-%{version}/extra/boost/boost_1_77_0/boost/
cp -r boost_1_77_0/boost/tti/ mysql-%{version}/extra/boost/boost_1_77_0/boost/
cp -r boost_1_77_0/boost/io/ mysql-%{version}/extra/boost/boost_1_77_0/boost/
cp -r boost_1_77_0/boost/random/ mysql-%{version}/extra/boost/boost_1_77_0/boost/
cp boost_1_77_0/boost/random.hpp mysql-%{version}/extra/boost/boost_1_77_0/boost/
```

