



# JWXT_GZHU

# GZHU 计算机科学与技术专业 软件方向课程设计

- Author: 浅若清风cyf
- Date: 2021/1/4-2021/1/11
- 博客：[GZHU软件方向综合课程设计——课程管理系统（Qt+mysql）_浅若清风cyf的博客-CSDN博客](https://blog.csdn.net/weixin_44002829/article/details/120773822)
- 数据库连接驱动问题见：[Qt客户端开发——与mysql数据库连接的驱动加载问题_浅若清风cyf的博客-CSDN博客](https://blog.csdn.net/weixin_44002829/article/details/120774004)
- 说明：此项目代码中已删除发送邮件的邮箱和token等敏感信息，重新上传的版本，因此没有开发过程的commit信息
- 本项目只在以下的开发环境中测试成功，其他环境自行测试

## 一、课程设计题目及内容

分组设计，按照软件工程思路设计简化的专业课数据库，尽量模拟现有专业课程一个学期的选课排课原型实际情况；
- 1．基本事实：

  ```
  (1)	学生只属于一个班级（如计科181）
  (2)	计科18级有6个班级，一个班有一个班主任，一个老师可能当多个班班主任
  (3)	学生上专业课有专业必修课，专业选修课两种（选修课不是所有人都选的，为简化同个班选修须一起上）
  (4)	不同班可能一起上课（如181，182合班上数据库）
  (5)	一个老师可以属于多个课程组，一个课程组包括多个老师，其中一个是课程负责人
  (6)	一个老师可以教多门课，一门课可能多个老师教（例如计算机导论是多个老师上）
  (7)	同一个班同一门课可能有多个老师教（如导论）
  (8)	一个老师可能教同一个班多门课 
  (9)	必修课必开；选修课不够人数就不开
  ```

  - 2．时间： 

  ```
  (1)	1-16周，周一到周五，1-9节； 课程安排的时间长度必须和课程学分一致
  (2)	同个班同个小节不能上多门课，不同班同门课可能一起上
  (3)	（同学继续补充细节）
  (4)	为减少工作量，不考虑教室安排，同时也不考虑上课人数限制
  (5)	为减少工作量，只考虑一个学期课程
  (6)	为减少工作量，不考虑全校必修课，全校选修课；只考虑本学院学生，只考虑本学院老师开课
  ```

- 3．用户：

  ```
  (1)	学生：自己个人选选修课，查自己个人课表，查自己个人分数，查自己绩点；
  (2)	任课教师（属于老师，只可以给任教的课程分数查询和修改）
  (3)	系主任（也是老师之一），可以查看所有学生、课程、老师，但是只能修改自己任教课程的分数
  ```

# 二、开发环境

```
①语言：C++
②开发框架：Qt5.9 (64bit)
③开发环境：Qt Creator 4.3.0
④编译器：MSVC 2017 64bit
⑤数据库：mysql
```
