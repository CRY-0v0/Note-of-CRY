# <center>峰值检测

###　电路图：

![alt text](AMP_cir.png)

###　仿真图：

A点

![alt text](AMP_A.png)

B点

![alt text](AMP_B.png)

A+B：

![alt text](AMP_AB.png)


###　理解

这个电路利用了两级电压跟随器，确保输入和输出。

其中，半波整流电路的原理：

输入为正时，D导通，C1储能。
输入为负时，由于第二级输入阻抗特别大，C1不放电，（D右边电势比左边高）D截止。

后级再加一个二阶低通，用于滤波