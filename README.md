# VINS-light
**描述**：
基于 VINS-Mono 框架，但不依赖 ROS, Ceres, G2O实现一个视觉惯性里程计。实现了基于 Eigen 的后端 LM 算法，滑动窗口算法，鲁棒核函数等等 SLAM 优化中常见的算法。
该代码支持 Ubuntu16/18

### 安装依赖项：

1. pangolin: <https://github.com/stevenlovegrove/Pangolin>

2. opencv

3. Eigen

4. Ceres: 仅在初始化部分使用了 ceres 做 sfm。

### 编译代码

```c++
cd VINS-light
mkdir build 
cd build
cmake ..
make -j4
```

### 运行
#### 1.曲线拟合示例
```c++
cd build
../bin/testCurveFitting 
```

#### 2. 在Euroc Dataset上的示例
```c++
cd build
../bin/run_euroc /home/dataset/EuRoC/MH-05/mav0/ ../config/
```
![vins](doc/vins.gif)

