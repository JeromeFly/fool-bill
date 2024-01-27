# fool-bill
呆头记账

```shell
# 消费方式
bill/assay GET
http://localhost:8082/api/bill/assay?date=2023-05&date_type=0&type=0
{"code":999,"message":"服务器异常，请联系后台管理人员","request":"GET：/api/bill/assay"}

# 收支走势
bill/line GET
http://localhost:8082/api/bill/line?date=2023-05


# 当月支出统计
bill/total_amount GET
http://localhost:8082/api/bill/total_amount?recordTime=2023-05
{"income":0,"consume":15.00,"budget":0,"balance":-15.00,"average":0.50}

# 记账记录
bill/all?recordTime= + data
http://localhost:8082/api/bill/all?recordTime=2023-05&start=0&count=10

# 删除记账
bill/remove POST

# 记账
bill/save POST
http://localhost:8082/api/bill/save
{"id":null,"amount":"15","type":0,"category_id":1,"remark":"早餐","record_time":"2023-05-21 20:53:34"}


# 导出账单
bill/export POST
http://localhost:8082/api/bill/export
{"code":999,"message":"服务器异常，请联系后台管理人员","request":"POST：/api/bill/export"}

# 设置预算
budget/save POST
http://localhost:8082/api/budget/save
{"date":"2023-05-21 20:56:55","amount":"200"}
{"success":true}

# 消费预算查询
budget/get GET
http://localhost:8082/api/budget/get?date=2023-05
{"current":15,"budget":0,"percent":100}

# 生成token
token POST
http://localhost:8082/api/token
{"account":"0c3jayFa1JsBlF07HFJa17RqDb3jayFl","type":0}
{"token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzY29wZSI6OCwiZXhwIjoxNjg0NjgwODE4LCJ1c2VySWQiOjUzNSwiaWF0IjoxNjg0NjczNjE4fQ.J4PF7q92XY_B5UIiqZnIzo6O326IUdyou_Fbicubwuc"}

# 校验token
token/verify POST

```
