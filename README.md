# Taichi-
一个基于 Taichi 语言 实现的轻量级实时光线追踪演示，支持 GPU 加速渲染、镜面反射、漫反射材质、硬阴影、棋盘格纹理和交互式光源控制。

## 特性
实时 GPU 渲染（自动适配 CUDA / Vulkan / Metal）
两种材质：漫反射（Diffuse）+ 镜面反射（Mirror）
真实硬阴影计算
无限棋盘格地板
可交互调节光源位置 & 光线反射次数
Whitted-style 光线追踪算法

## 快速开始
1. 安装依赖
```bash
pip install taichi
```
2. 运行代码
直接运行 Python 文件即可启动渲染窗口：
```bash
python raytracer.py
```
3. 交互控制
右侧控制面板支持实时调节：
Light X/Y/Z：光源三维位置
Max Bounces：光线最大反射次数（1~5）

## 核心实现
光线 - 物体求交：球体 + 无限平面
光照模型：环境光 + 漫反射
阴影：阴影射线检测遮挡
防自相交：法线方向微小偏移
迭代式光线弹射：支持多级镜面反射

## 效果预览
<img width="640" height="511" alt="0hjq9F7O_converted" src="https://github.com/user-attachments/assets/8837908f-2e46-4970-8d75-6aabe8e22b45" />
