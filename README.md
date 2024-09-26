## 本项目实现的最终作用是基于SSM公司员工管理系统
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 员工管理
 - 管理员登陆
 - 职位管理
 - 部门管理
### 第2个角色为用户角色，实现了如下功能：
 - 员工查看
 - 查看职位
 - 部门查看
## 数据库设计如下：
# 数据库设计文档

**数据库名：** ssm_company_yg_sys

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [admin](#admin) | 管理员表 |
| [t_department](#t_department) |  |
| [t_employee](#t_employee) |  |
| [t_position](#t_position) |  |

**表名：** <a id="admin">admin</a>

**说明：** 管理员表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | username |   varchar   | 255 |   0    |    N     |  Y   |   ''    | 日期  |
|  2   | PASSWORD |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |

**表名：** <a id="t_department">t_department</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | departmentNo |   varchar   | 255 |   0    |    N     |  Y   |       | departmentNo  |
|  2   | departmentName |   varchar   | 255 |   0    |    N     |  N   |       | 部门名称  |

**表名：** <a id="t_employee">t_employee</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | employeeNo |   varchar   | 255 |   0    |    N     |  Y   |       | employeeNo  |
|  2   | positionObj |   int   | 10 |   0    |    N     |  N   |       | 职位  |
|  3   | name |   varchar   | 255 |   0    |    N     |  N   |       | 姓名  |
|  4   | sex |   varchar   | 4 |   0    |    N     |  N   |       | 性别  |
|  5   | employeePhoto |   varchar   | 60 |   0    |    N     |  N   |       | 员工照片  |
|  6   | birthday |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 出生日期  |
|  7   | schoolRecord |   varchar   | 255 |   0    |    N     |  N   |       | 学历  |
|  8   | employeeDesc |   varchar   | 5000 |   0    |    Y     |  N   |   NULL    | 员工介绍  |

**表名：** <a id="t_position">t_position</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | positionId |   int   | 10 |   0    |    N     |  Y   |       | 职位id  |
|  2   | departmentObj |   varchar   | 255 |   0    |    N     |  N   |       | 所属部门  |
|  3   | positionName |   varchar   | 255 |   0    |    N     |  N   |       | 职位名称  |
|  4   | baseSalary |   float   | 13 |   0    |    N     |  N   |       | 基本工资  |
|  5   | sellPercent |   varchar   | 255 |   0    |    N     |  N   |       | 销售提成  |

