# 一级标题
## 二级标题
```sql
--备份数据表
create table orders_info_20231201_bak as select * from yueran_202311.orders_info_20231201;
--给数据表添加字段
alter table orders_info_20231201 add COLUMN id int,
--从备份表中恢复数据到正式表
insert into orders_info_20231201 (id,account,strategy_id,job_id,task_id,order_id,remote_order_id,symbol,direction.price.volume,state) select () from  orders_info_20231201_bak;

```
