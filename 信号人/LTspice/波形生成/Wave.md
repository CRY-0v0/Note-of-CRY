# <center>波形配置

信号源功能选择PULSE

## 参数说明：


- #### Vinitial[V]
最低电压

- #### Von[V]
最高电压

- #### Tdelay[s]
输出延迟(n秒后输出波形)

- #### Trise[s]
上升时间（上升沿占用时间）

- #### Tfall[s]
下降时间（下降沿占用时间）

- #### Ton[s]
开启时间（高电平保持时间）

- #### Tperiod[s]
一整个周期持续时间（Trise + Tfall + Ton）

- #### Ncycles
多少周期（生成多少周期，默认不填，一直生成）


>波形关键参数：
- Trise[s]
- Tfall[s]
- Ton[s]
- Tperiod[s]
> 上升沿和下降沿最好给一点时间，不然容易报错；
> 高电平时间可以为0
> Tperiod 时间算好，不要给少

以下参数说明（x：控制值；y 非常小的值）
$$f = \frac{1}{Tperiod}$$

## 三角波

- Trise[s]      = x
- Tfall[s]      = x
- Ton[s]        = 0
- Tperiod[s]    = 2x

## 方波

- Trise[s]      = y
- Tfall[s]      = y
- Ton[s]        = x
- Tperiod[s]    = 2x + 2y













