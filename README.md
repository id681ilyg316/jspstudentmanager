## 本项目实现的最终作用是基于JSP学生信息管理系统
## 分为3个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 增删改查学生
 - 学生成绩查询
 - 教师增删改查
 - 教师查询
 - 添加学生
 - 管理员首页
### 第2个角色为教师角色，实现了如下功能：
 - 修改学生成绩
 - 学生信息查找
 - 教师资料修改
 - 查找学生成绩
### 第3个角色为学生角色，实现了如下功能：
 - 修改个人资料
 - 按照条件查询自己的成绩
 - 查询自己的成绩
## 数据库设计如下：
# 数据库设计文档

**数据库名：** studentmanager

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [cla2sub](#cla2sub) |  |
| [classes](#classes) |  |
| [major](#major) |  |
| [operator](#operator) |  |
| [privilege](#privilege) |  |
| [role](#role) | 角色表 |
| [score](#score) |  |
| [student](#student) | 学生信息表 |
| [subject](#subject) |  |
| [teacher](#teacher) | 教师信息表 |

**表名：** <a id="cla2sub">cla2sub</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | cla2sub_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | cla_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | sub_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  4   | tec_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="classes">classes</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | cla_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | cla_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  3   | maj_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  4   | cla_tec |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="major">major</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | maj_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | maj_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  3   | maj_prin |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  4   | maj_link |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  5   | maj_phone |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="operator">operator</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ope_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | ope_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  3   | ope_pwd |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  4   | rol_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="privilege">privilege</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | pri_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | pri_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  3   | pri_url |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | menu_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    | 菜单名称  |
|  5   | rol_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="role">role</a>

**说明：** 角色表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | rol_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | rol_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="score">score</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | sco_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | sco_daily |   float   | 13 |   0    |    Y     |  N   |   0    |   |
|  3   | sco_exam |   float   | 13 |   0    |    Y     |  N   |   0    |   |
|  4   | sco_count |   float   | 13 |   0    |    Y     |  N   |   0    |   |
|  5   | stu_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 学生ID  |
|  6   | sub_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | cla2sub_id |   int   | 10 |   0    |    N     |  N   |       |   |
|  8   | cla_id |   int   | 10 |   0    |    N     |  N   |       |   |

**表名：** <a id="student">student</a>

**说明：** 学生信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | stu_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | ope_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | stu_no |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  4   | stu_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  5   | stu_sex |   enum   | 1 |   0    |    Y     |  N   |   '男'    |   |
|  6   | stu_birth |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | stu_pic |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  8   | cla_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="subject">subject</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | sub_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | sub_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  3   | sub_type |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  4   | sub_times |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="teacher">teacher</a>

**说明：** 教师信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | tec_id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | ope_id |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  3   | tec_name |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  4   | tec_birth |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  5   | tec_sex |   enum   | 1 |   0    |    Y     |  N   |   '男'    |   |
|  6   | tec_major |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |
|  7   | tec_phone |   varchar   | 22 |   0    |    Y     |  N   |   NULL    |   |

**运行不出来可以微信 javape 我的公众号：源码码头**
