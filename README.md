# 同步 Buck/Boost 变换器学习项目

本项目是同步 Buck/Boost 双向 DC-DC 变换器的学习记录，涵盖理论分析、仿真建模、硬件设计和控制策略实现。

## 项目结构

### 0. Notes - 学习笔记

| 文件名 | 内容 |
|--------|------|
| Sync buckbost notes.md | 完整学习笔记，包含理论基础、硬件计算、控制策略、系统辨识等内容 |
| Sync buckbost notes_images/ | 笔记配图文件夹 |

主要内容：
- Buck/Boost 拓扑理论基础与稳态分析
- 硬件参数计算与器件选型
- 开发板原理图分析（主功率板、控制板、驱动电路、调理电路）
- PID 控制器设计与频域补偿
- 系统辨识与 Bode 图拟合
- Type 3 补偿器设计

### 1. SimulationModel - 仿真模型

| 文件名 | 内容 |
|--------|------|
| buck.slx | Buck 降压变换器开环仿真模型 |
| sync_buck.slx | 同步 Buck 降压变换器仿真模型 |
| sync_boost.slx | 同步 Boost 升压变换器仿真模型 |
| Buck_P_control.slx | Buck 比例控制器仿真模型 |
| Buck_PID_control.slx | Buck PID 控制器仿真模型 |
| Boost_PID_control.slx | Boost PID 控制器仿真模型 |
| Buck_Simulated_calibration.slx | Buck 定标原理仿真 |
| Boost_Simulated_calibration.slx | Boost 定标原理仿真 |
| Buck_Systematic_identification.slx | Buck 系统辨识仿真 |
| Average_Current_Mode.slx | 平均电流模式控制仿真 |

### 2. BoardAnalysis - 硬件分析

| 文件名 | 内容 |
|--------|------|
| 开发板关系系统框图.vsdx | 开发板硬件关系系统框图源文件（Visio） |
| 开发板关系系统框图.png | 开发板硬件关系系统框图（PNG 格式） |

硬件系统包含：
- 主功率板（主电路、驱动电路、调理电路、辅助电源）
- 控制板（STM32 控制器、ADC 采样、PWM 输出）
- 信号流向与接口定义

### 3. 工具

| 文件名 | 内容 |
|--------|------|
| bode-viewer.html | 典型环节 Bode 图交互式查看器 |

## 技术要点

- 电力电子拓扑工作原理与稳态分析方法
- 同步整流技术（用 MOS 管代替续流二极管降低损耗）
- 数字化定标技术（Q12 格式 ADC 采样）
- 频域补偿法设计 PID 控制器
- 相位裕度与穿越频率的工程设计
- 系统辨识与传递函数拟合

## 开发环境

- MATLAB/Simulink（电力电子仿真）
- STM32 单片机（数字控制实现）
- Visio（系统框图绘制）
