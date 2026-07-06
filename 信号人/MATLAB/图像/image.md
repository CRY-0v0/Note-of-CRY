# <center>图像输出


### 简单
```
x = 0:0.1:2*pi;

plot(x, sin(x));

title('正弦曲线');


```

### 函数

```
% 定义函数
f = @(x) 1./(2*x - 1);

% 使用 fplot 绘制，它能自动处理奇点，避免连接无穷大
figure;
fplot(f, [-10, 10], 'LineWidth', 1.5);

% 添加网格、标题和轴标签
grid on;
xlabel('x');
ylabel('y');
title('y = 1 / (2x - 1)');

% 设置 y 轴范围，避免无穷大使得图形压缩
ylim([-10, 10]);  % 可根据需要调整

% 可选：标记渐近线位置
hold on;
xline(0.5, '--r', 'x = 0.5');  % 垂直渐近线
hold off;

% 保存图像（如果需要）
exportgraphics(gcf, 'function_plot.png', 'Resolution', 300);
```


