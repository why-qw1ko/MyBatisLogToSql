# MyBatisLogToSql
> mybatis的日志转正常可用sql的工具
> 支持--开头，中文结尾的注释
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

