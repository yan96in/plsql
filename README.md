# plsql
#### 一、pl/sql概念
	1. pl/sql架构
		a. pl/sql架构
		b. pl/sql块结构
		c. pl/sql是如何执行的
	2. pl/sql开发环境
		a. sql developer
		b. 执行pl/sql脚本
	3. pl/sql基础知识
		dbms_output.put_line语句
		替代变量功能
#### 二、pl/sql编程基础
	1. pl/sql语言组件
	2. pl/sql变量
	3. pl/sql保留字
	4. pl/sql中的标识符
	5. 挂靠的数据类型
	6. 声明和初始化便利
	7. 块作用域、嵌套块和标签
#### 三、在pl/sql中的sql
	1. 在pl/sql中的dml语句
		a. 使用select into初始化变量
		b. 使用变量初始化的select into语法
		c. 在pl/sql块中使用dml
		d. 在pl/sql块中使用序列
	2. 在pl/sql中的事务控制
		a. 使用commit、rollback和savepoint
		b. 将dml和事务控制相结合
#### 四、条件控制
	1. if语句
		a. if-then语句
		b. if-then-else语句
		c. elsif语句
		d. 嵌套的if语句
	2. case语句
		a. case语句
		b. case表达式
		c. nullif和coalesce函数
			i. nullif函数
			ii. coalsce函数
#### 五、迭代控制
	1. 简单循环
		a. exit语句
		b. exit when语句
	2. while循环
		a. 使用while循环
		b. 提前终止while循环
	3. 数字for循环
		a. 在循环中使用in选项
		b. 在循环中使用reverse选项
		c. 提前终止数字for循环
	4. continue语句
		a. 使用continue语句
		b. continue when语句
	5. 嵌套循环
		a. 使用
		b. 使用循环标签
#### 六、错误处理和内置异常
	1. 处理错误
	2. 内置异常
	3. 异常作用域
	4. 用户定义的异常
	5. 异常传播
	6. raise_application_error
	7. exception_init编译指示
	8. sqlcode和sqlerrm
#### 七、游标简介
	1. 游标类型
		a. 隐式油表
		b. 显式游标
	2. 游标循环
		a. 处理显式游标
		b. 使用用户定义的记录
		c. 使用游标属性
	3. 游标for循环
	4. 嵌套游标
	5. 参数化游标
	6. 复杂的嵌套游标
	7. for update和where current游标
#### 八、触发器
	1. 概念
		a. 数据库触发器
		b. before触发器
		c. after触发器
		d. 自治事务
	2. 类型
		a. 行触发器和语句触发器
		b. instead of触发器
	3. 变异表
		a. 变异表问题
		b. 复合触发器
#### 九、集合
	1. Pl/sql表
		a. 关联数组
		b. 嵌套表
		c. 集合方法
			i. EXISTS
			ii. COUNT
			iii. EXTEND
			iv. DELETE
			v. FIRST和LAST
			vi. PRIOR和NEXT
			vii. TRIM
	2. 变长数组
	集合	元素个数	索引	声明时的状态	可被定义	致密或稀疏
	关联数组	未设置	字符串或PLS_	清空的	在pl/sql块\包\过程	二者皆可
			INTEGER		或函数中
	嵌套表	未设置	INTEGER	NULL	在pl/sql块\包\过程或函数	开始时致密,
					中,并在模式级别作为独立类型	但可以变稀疏
	变长数组	在声明时设置	INTEGER	NULL	在pl/sql块\包\过程或函数	总是致密
					中,并在模式级别作为独立
					类型
	3. 多级集合
#### 十、记录
	1. 记录类型
		a. 基于表和基于游标的记录
		b. 用户定义的记录
		c. 记录兼容性
	2. 嵌套记录
	3. 记录集合
#### 十一、本地动态sql
	1. execute immediate语句
		a. 使用
		b. 避免使用时的常见ora错误
	2. open-for、fetch和close语句
		a. 打开游标
		b. 从游标中读取
		c. 关闭游标
#### 十二、批量sql
	1. forall语句
		a. 使用
		b. save exceptions选项
		c. indices of选项
		d. values of选项
	2. bulk collect子句
	3. 在sql中绑定集合
		a. 将集合与execute immediate语句绑定
		b. 将集合与open-for、fetch和close绑定
#### 十三、存储过程
	1. 模块化代码的好处
		a. 块结构
		b. 匿名块
	2. 创建过程
		a. 示例
		b. 查询数据字典来获取过程的信息
	3. 传递的过程参数in和out
#### 十四、函数
	1. 创建和使用
	2. 在sql语句中使用
	3. 在sql中优化函数执行
		a. 使用with子句定义函数
		b. 使用udf编译指示创建函数
#### 十五、包
	1. 创建
		a. 规范
		b. 创建包体
		c. 调用已存储的包
		d. 创建私有对象
	2. 游标变量
	3. 扩展包
	4. 包的实例化和初始化
	5. serially_reusable包
#### 十六、存储代码
	1. 收集存储代码的相关信息
		a. 从数据字典获取代码的信息
		b. 重载模块
#### 十七、oracle对象类型
	1. 对象类型
		a. 创建
		b. 使用对象类型和集合
	2. 对象类型的方法
		a. 构造方法
		b. 成员方法
		c. 静态方法
		d. 比较对象
#### 十八、oracle提供的包
	1. 利用oracle提供的包扩展功能
		a. 在pl/sql中利用utl_file访问文件
		b. 利用gdbms_job调度作业
		c. 利用dbms_xplan生成解释计划
		d. 利用dbms_sql产生隐式语句结果
	2. 利用oracle提供的包报告错误
		a. dbms_utility包
		b. utl_call_stack
#### 十九、优化pl/sql
	1. 调优工具
		a. 剖析器api
		b. 跟踪api
		c. 层次式剖析器
	2. pl/sql优化级别
	3. 子程序内联
	4. 2016/12/13 
