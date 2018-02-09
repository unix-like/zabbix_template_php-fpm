# zabbix_template_php-fpm

| item                         | trigger                                           |
| :--------------------------: | :-----------------------------------------------: |
| php-fpm accepted connection  |                                                   |
| php-fpm active processes     | php-fpm active processes to high on {HOST.NAME}   |
| php-fpm idle processes       |                                                   |
| php-fpm listen queue         |                                                   |
| php-fpm listen queue length  |                                                   |
| php-fpm max active processes |                                                   |
| php-fpm  server is running   | php-fpm server is down on {HOST.NAME}             |
| php-fpm total processes      |                                                   |
| php-fpm max children reached |                                                   |
| php-fpm max listen queue     |                                                   |
| php-fpm slow requests        |                                                   |

适用于zabbix3.4及以上版本,此监控项目共包含2个文件:

1. userparameter_php.conf
2. phpfpm_status.conf
3. php.xml

其中`userparameter_php.conf`, `phpfpm_status.conf`需要分发到各个php服务器上，`php.xml`作为模版文件导入zabbix中。

在导入模板之后需要修改两个个“宏”的值:
1. {$PHPFPM_PORT}
2. {$PHPFPM_SERVER}

为对应的php-fpm状态监听端口和地址。
