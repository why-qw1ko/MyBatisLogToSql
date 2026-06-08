# MyBatisLogToSql
> **mybatis的日志转正常可用sql的小工具**
>
> 支持`--`开头，`中文`结尾的注释
>
> 业务复杂的sql我测的也没问题，有问题可以直接提issue
>
> 直接使用`MyBatisLogToSql.html`即可，如果觉得好用，欢迎给个star
------
例如输入
```sql
==>  Preparing: SELECT --测试注释 uid,name,password,mail,url,screenName,created,activated,logged,`group` --测试注释 FROM typecho_users WHERE uid=?
==> Parameters: 1(Long)
<==    Columns: uid, name, password, mail, url, screenName, created, activated, logged, group
<==        Row: 1, 不冷, $P$B.wp5CtZSMwetq9aGCFI8QSGM9NFy40, 11@qq.com, https://www.buleng.xyz/, 不冷, 1598017815, 1769073410, 1769073369, administrator
<==      Total: 1
```
解析结果
```sql
SELECT uid,name,password,mail,url,screenName,created,activated,logged,`group` FROM typecho_users WHERE uid=1;
```

