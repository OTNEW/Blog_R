# R导入和导出.xls文件

# xlsx 包的使用

*首先要注意，xlsx包要依赖JAVA，所以在使用该包之前，要先安装好JAVA，配置好JAVA环境*

## 安装

**直接用install.packages("xlsx")安装**

## 使用

**write.xlsx(data, "fileLocate/data.xls", sheetName = "data_1", append = TRUE)** *设置参数 append = TRUE，可以在一张Excel表格上插入多个sheet*

## 使用情况

**避免导出csv格式时，由于不能修改分隔符（sep），而导致的最终文件格式分割错误**

## 缺点

由于Excel有时候会自动将一些数据格式转换成日期，所以导出完毕之后要记得检查，更改数据类型

# readxl 包的使用

*该包的依赖较少*

## 安装

install.packages()

## 使用

read_excel(path, sheet = 1, col_names = TRUE, col_types = NULL, na = "", skip = 0)

* sheet	输入sheet的名称或序号，默认为第一张
* col_name    TRUE是指第一行作为列名，FALSE指无列名
* col_types    输入表格的类型
* na    missing value，输入特定值可以替代na
* skip    跳过前几行不作读取

