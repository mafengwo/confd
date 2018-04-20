# confd

Forked from https://github.com/kelseyhightower/confd


## 改进
```
/*
 * 完成confd前的任务：根据etcd中的namespace将对应的标准配置文件和标准模版文件中的变量替换掉
 * 1.根据特殊的命名规则检查标准配置文件和模版文件是否存在
 * 2.用namespace替换变量生成一对临时的配置文件和模版文件，判断是否一样。如果不一样，替换成新的配置文件和模版文件
 *
 * 命令规范:
 * namespace - es-XXX-data, es-XXX-master, redis, memcached. 
 (注：es-XXX-data和es-XXX-master只需生成一对配置文件和模版文件)(服务-业务-data || 服务-业务-master)
 * 标准配置文件 - es.tomlx, redis.tomlx(命名空间的替换词为 __NS__)
 * 标准模版文件 - es.tmplx, redis.tmplx(命名空间的替换词为 __NS__)
 * 配置文件 - es-XXX.toml
 * 模版文件 - es-XXX-tmpl
 */
```
