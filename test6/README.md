# 实验6：基于GitHub的实验管理平台的分析与设计
|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|:---:|
|201510414119|软件(本)15-1|汪俊程|![flow1](wc3.jpg)|

## 1. 概述
- 基于GitHub的实验管理平台的作用是在线管理实验成绩的Web应用系统。学生和老师的实验内容均存放在GitHUB
页面上。
- 学生的功能主要有：一是设置自己的GitHub用户名，二是查询自己的实验成绩。学生的GitHub用户名是公开的，但成绩不公开。
- 老师的功能主要有：一是批改每个学生的成绩，二是查看每个学生的成绩。
- 老师和学生都能通过本系统的链接方便地跳转到学生的每个GitHUB实验目录，以便批改实验或者查看实验情况。
- 实验成绩按数字分数计算，每项实验的满分为100分，最低为0分。
- 系统自动计算每个学生的所有实验的平均分。

## 2. 系统总体结构
![flow1](png1.png)

## 3. 用例图设计 [源码](./src/usecase.puml)
![](./img/usecase.png)

## 4. 类图设计 [源码](./src/class.puml)
![](./img/class.png)

## 5. 数据库设计
- ### [参见数据库设计](./数据库设计.md)

## 6. 用例及界面详细设计

- ### [“登录”用例](./src/yongli/登录.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/login_html.html)
- ### [“登出”用例](./src/yongli/退出.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-student_html.html)
- ### [“查看用户信息”用例](./src/yongli/查看用户信息.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-student_html.html)
- ### [“修改用户信息”用例](./src/yongli/修改用户信息.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-student_html.html)
- ### [“修改密码”用例](./src/yongli/修改密码.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-student_html.html)
- ### [“选择学期”用例](./src/yongli/选择学期.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-teacher_html.html)
- ### [“选择课程”用例](./src/yongli/选择课程.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-teacher_html.html)
- ### [“查看成绩”用例](./src/yongli/查看成绩.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-student_html.html)
- ### [“选课查询”用例](./src/yongli/选课查询.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/index-student_html.html)
- ### [“发布实验”用例](./src/yongli/发布实验.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/publishtest_html.html)
- ### [“提交实验作业”用例](./src/yongli/提交实验作业.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/publishtest_html.html)
- ### [“评定成绩”用例](./src/yongli/评定成绩.md),[界面](https://guokunjin.github.io/is_analysis/test6/ui/publishtest_html.html)







