
# 实验4：图书管理系统顺序图绘制
|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|:---:|
|201510414119|软件(本)15-1|汪俊程|![flow1](wc3.jpg)|

## 图书管理系统的顺序图

## 1. 借书用例
## 1.1. 借书用例PlantUML源码

``` sequence
@startuml
actor  借阅者 as reader
actor  图书管理员 as admin
activate reader
activate admin
reader->admin:提供需借书籍
reader->admin:提供借书卡号
deactivate reader
admin->图书管理系统:登录
activate 图书管理系统
admin<-图书管理系统:读者信息
  图书管理系统->读者:图书信息
activate 读者
deactivate 读者
图书管理系统->book:图书信息
activate book
deactivate book
图书管理系统->读者:借书
activate 读者
deactivate 读者
图书管理系统->借书记录:创建借书信息
activate 借书记录
deactivate 借书记录
图书管理系统->book:更改图书数据信息
activate book
deactivate book
图书管理系统->读者:更改图书数据信息
activate 读者
deactivate 读者
图书管理系统-->admin:借书
deactivate 图书管理系统
admin-->reader:借阅成功
activate reader
deactivate reader
deactivate admin
@enduml

```

## 1.2. 借书用例顺序图
![class](wc1.png)

## 1.3. 借书用例顺序图说明
```
1. login()：借阅者把需借图书和借书卡号提供给图书管理员，图书管理员登陆图书管理系统函数。
2. showReaderInfo()：登录系统后通过借书卡号显示该借阅者的信息函数。
3. check()：检查该借阅者的合法性函数。
4. getReaderInfo()：获取读者的相关信息函数。
5. check()：检查该读者的借书限额，是否超限的函数。
6. getBookInfo()：获取需借图书的相关信息函数。
7. borrow()：借阅者的借书函数。
8. builtBookInfo()：创建借书记录的函数。
9. updateBookInfo()：更新图书信息的函数，标记该图书的状态为已借。
10. updateReaderInfo()：更新读者的借书信息函数。
11. isBorrow()：借阅成功的函数。
  ```

## 2. 还书用例
## 2.1. 还书用例PlantUML源码

``` sequence
@startuml
actor  借阅者 as reader
actor  图书管理员 as admin
activate reader
activate admin
reader->admin:   还书书籍
deactivate reader
admin->admin:检查是否损坏书籍
admin->图书管理系统:登录
activate 图书管理系统
图书管理系统->book:图书信息
activate book
deactivate book
图书管理系统->借书记录:图书信息
activate 借书记录
图书管理系统->借书记录:借书日期
图书管理系统->借书记录:还书日期
图书管理系统->借书记录:是否逾期
deactivate 借书记录
图书管理系统->还书记录:创建还书信息
activate 还书记录
deactivate 还书记录
图书管理系统->book:更新还书信息
activate book
deactivate book
图书管理系统->读者:更新还书信息
activate 读者
deactivate 读者
图书管理系统->逾期记录:记录
activate 逾期记录
deactivate 逾期记录
图书管理系统-->admin:还书
deactivate 图书管理系统
admin-->reader:还书成功
activate reader
deactivate reader
deactivate admin
@enduml
```

## 2.2. 还书用例顺序图
![class](wc2.png)

## 2.3. 还书用例顺序图说明
```
1. login()：借阅者提供还书书籍，管理员登陆该系统的函数。
2. getBookInfo()：扫描该书籍的书号，获取相关图书信息的函数。
3. getBorrowInfo()：获取借阅记录的信息的函数。
4. getBorrowDate()：获取借阅该书籍的日期的函数。
5. getNowDate()：获取当前时间的日期的函数。
6. isOverTime()：判断该借阅者的借书时间是否超时的函数。
7. builtReturnInfo()：创建还书记录的函数。
8. updateBookInfo()：更新图书馆里的书籍信息的函数，标记该图书的状态为可借。
9. updateReaderInfo()：更新读者的还书信息的函数。
10. record()：记录借阅者的逾期记录的函数。
11. return：返回还书成功。
```
