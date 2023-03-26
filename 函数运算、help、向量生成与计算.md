# MATLAB语法
## MATLAB函数运算、help、向量生成与计算
---
### MATLAB函数计算
>除了简单的依靠运算符进行的MATLAB四则运算等，MATLAB还包括复数运算、三角函数和指数运算等运算   

**·MATLAB提供的复数函数**
```matlab
Abs:模
Angle:复数的相角
complex:用实部和虚部构造一个复数
conj:复数的共轭
imag:复数的虚部
real:复数的实部
unwrap:调整矩阵元素的相位
isreal:是否为实数矩阵
cplxpair:把复数矩阵排列成复共轭对
```
**·三角函数**
```matlab
正弦函数sin       sin    a/c
反正弦函数arcsin  asin   /
余弦函数cos       cos    b/c
反余弦arccos      acos   /
正切函数tangent   tan    a/b
反正切函数arctan  atan    /
余切函数cotangent cot    b/a
正割函数secant    sec    c/b
余割函数cosecant  csc    c/a
其他的反函数同理
```
---
### MATLAB向量生成
>1.直接输入生成向量(同矩阵)  

>2.冒号法（适用于有规律的向量）
```matlab
基本格式:x=first:increment:last,表示创建一个从first开始，知道last结束，数据元素增量为increment的向量。
若增量为1，上面创建向量的方式简写为x=first:last。
```
>3.利用函数linspace创建向量  
linspace通过直接定义数据元素个数，而不是数据元素之间的增量来创建向量。此函数的调用格式如下。
```matlab
linspace(first_value,last_value,number)
该调用格式表示创建一个从first_value开始last_value结束，包含number个元素的向量.

%举个例子
>>linsapce(1,7,5)
a=1.0000 2.5000 4.0000 5.5000 7.0000   %会均分这段长度
```
---
### 向量引用
```
x(n)           表示向量x中的第n个元素
x(n1:n2)       表示向量中的第n1至n2个元素
```
---
### 向量的点积运算
>对于向量a、b，其点积可以利用a.*b得到，也可以直接用命令dot算出，该命令的调用格式见表
```matlab
dot(a,b)       %返回向量a和b的点积，需要说明的的是，a和b必须同维。另外，当a、b都是列向量时，dot(a,b)等同于a.*b
dot(a,b,dim)   %返回向量a和b在dim维的点积
```
---
### 向量的叉积运算
>在空间解析几何学中，两个向量叉乘的结果是一个过两相交向量交点且垂直于两向量所在平面的向量。在MATLAB中，向量的叉积运算可由函数corss来实现
```
cross(a,b)      %返回向量a和b的叉积，需要说明的是，a和b必须实三维的向量
cross(a,b,dim)  %返回向量a和b在dim维的叉积。需要说明的是，a和b必须有相同的维数，size(a,dim)和size(b,dim)的结果必须为3
```
