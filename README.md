# 车牌自动检测系统

## 介绍
该车牌检测系统基于YOLO算法
参考论文如下
* Paper webpage: http://sergiomsilva.com/pubs/alpr-unconstrained/


## 运行环境

运行代码之前，首先安装带有TensorFlow后端的Keras框架。Darknet框架是独立的，位于“ darknet”文件夹中，必须在运行测试之前进行编译。要构建Darknet，只需在“ darknet”文件夹中键入“ make”：

$ cd darknet && make

**当前版本已在Ubuntu 18.04计算机，Keras 2.2.4，TensorFlow 1.5.0，OpenCV 2.4.9，NumPy 1.14和Python 2.7上进行了测试。**


## 简单运行此项目

使用脚本“ run.sh”运行系统时，它需要3个参数：
输入目录（-i）：至少应包含1张JPG或PNG格式的图像；
输出目录（-o）：在识别过程中，许多临时文件将在此目录内生成并最终删除。其余文件将与自动注释的图像相关；
CSV文件（-c）：指定输出CSV文件。
```shellscript
$ bash get-networks.sh && bash run.sh -i samples/test -o /tmp/output -c /tmp/output/results.csv
```


