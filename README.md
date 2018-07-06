参考：
https://github.com/lafitehhq/RAM-JD

使用说明：
>> git clone https://github.com/LewisTian/RAM-JD.git
>> cd RAM-JD
>> pip install -r requirements.txt


1.建表
```
mysql>  create database yanwo character set utf8;
mysql>  create database yanwoyuanzhan character set utf8;
mysql>  create database jishiyanwo character set utf8;
```
2.创建字段
```
mysql>  use yanwo/yanwoyuanzhan/jishiyanwo;
mysql>  CREATE TABLE yanwo/yanwoyuanzhan/jishiyanwo(
           id INT PRIMARY KEY AUTO_INCREMENT,
           name VARCHAR(255),
           price VARCHAR(45),
           shop VARCHAR(45),
           comments VARCHAR(45),
           href VARCHAR(45));
```

3.运行脚本
```    
>> python ram.py
```

4.导出数据表
```
mysql>  SELECT * FROM ram  r where r.comments LIKE '%万+' ORDER BY CAST(r.comments AS DECIMAL) DESC LIMIT 500;
mysql>  SELECT * FROM ram  r where r.comments ORDER BY CAST (r.comments AS DECIMAL) DESC ;
```

5.清空数据表
```
mysql> truncate table ram;
```

