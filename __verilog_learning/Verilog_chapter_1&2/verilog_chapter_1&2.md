# Verilog Learning Chapter 1&2 
----------------------
In this chapter, we would focus on fundamentals and core concepts of Verilog HDL. 在这一章中，主要介绍一些概念和Verlog HDL的基础知识。

### 0.模块概念：

- 软核 Soft core: 
	一般指经过功能验证，可综合的Verilog HDL（VHDL）模型.

- 固核 Firm core: 
	通知指在ASIC or FPGA 器件上，经过综合验证的电路网表文件。

- 硬核 Hard core:
	在ASIC器件上，经过验证正确的的电路结构版图掩膜。

### 1.Verilog HDL 基础

- 数值状态

[vaule_conditions](https://github.com/XuLixing/Note/raw/main/images)

- 位制：二进制 b； 八进制: o；十进制：d；十六进制：h
- 整数表示 8‘b0000_0001。 位数‘位制‘数字

### 2. 数据类型

- 分类：wire（tri三态门，tri0下拉电阻，tri1上拉电阻），reg，RAM
- reg：对应硬件电路元件具有状态保持作用；触发器，锁存器
- RAM：类似于二维数组的定义方式。 reg[7:0] mem1[255:0] //定义256个8位寄存器的mem。

抽象数据类型：

- 整型 integer，时间 time，实型 real ，参数型parameter.
- integer index //定义32位有符号数
- time a; // 定义两个64位的时间型变量。 
主要用于对模拟时间的存储和计算处理，常与$time 一起使用
- real stime; // 定义一个实数型数据（浮点型），常用于延迟时间的计算
- parameter length=32, // 常量，在仿真之前就被复制，提高程序可读性。

运算符：
[opeartors]()

#### _Note_:
赋值语句下，结果的长度是由操作左端目标长度决定。取低N位，不够补0。

### 3. 条件运算符

example: (!sel)?in1:in2;

### 4. 连接和复制运算符
[连接]()

### 5. 模块的基本概念

Module是verilog HDL的基本单元
> 组成：

- 开始：NAME module；- endmodule
- 端口定义：input output （模块引用具体）
- 数据类型定义： wire，reg，memory，parameter
- 逻辑功能描述：initial，always，assign，function，task

