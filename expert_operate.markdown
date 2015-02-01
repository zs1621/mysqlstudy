##to continue...


 - **caculate few fields in one table in a word**
  - 当你做数据库重构时，对多个字段进行计算，然后将最后的值赋给同表的另外一个字段时

```
UPDATE profiles as p JOIN (SELECT l.user_id, COUNT(*) as lscount FROM lu as l where NOT (l.deleted=1)) AS r ON p.user_id = r.user_id SET p.lu_count= r.lscount;
```
