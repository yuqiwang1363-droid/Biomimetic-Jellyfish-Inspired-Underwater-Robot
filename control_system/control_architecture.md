# Control System Architecture

## Overview

The control system coordinates propulsion, steering, and timing
to enable stable and controllable underwater motion of the biomimetic jellyfish-inspired robot.

Rather than complex closed-loop control,
the system adopts a **time-based and event-driven control architecture**
suitable for early-stage prototyping and experimental validation.

---

## System Components

The control system consists of the following key elements:

- Microcontroller unit (MCU)
- Actuators for propulsion and steering
- Power management subsystem
- Optional sensors for future expansion

---

## Control Strategy

### Open-Loop Pulsed Control

The propulsion mechanism operates using a periodic pulsed control scheme.

Each propulsion cycle consists of:

1. **Contraction Phase**  
   The elastic chamber contracts, expelling water and generating thrust.

2. **Relaxation Phase**  
   The chamber expands, refilling with water in preparation for the next cycle.

The timing of these phases is controlled by the MCU
through predefined duty cycles and frequency settings.

---

### Steering Control Integration

Steering commands are implemented by adjusting the deflection angle
of the flow-guiding mechanism.

During propulsion cycles:

- Steering angle remains fixed for straight motion
- Steering angle is biased to one side for turning
- Continuous adjustment enables curved trajectories

The steering actuator is synchronized with the propulsion cycle
to ensure smooth and stable motion.

---

## Control Flow

The high-level control logic follows the sequence:

1. Initialize system and actuators
2. Set propulsion cycle parameters (frequency, duration)
3. Set steering deflection angle
4. Execute propulsion-steering cycle
5. Repeat until stop command or power-down

---

## Timing and Synchronization

Accurate timing is essential for stable motion.

The controller ensures:

- Consistent propulsion cycle frequency
- Proper phase alignment between propulsion and steering
- Smooth transitions between motion states

This approach minimizes mechanical stress
and improves repeatability of motion.

---

## Control Modes

The system supports multiple operating modes:

- **Forward Cruise Mode**  
  Constant propulsion frequency with zero steering offset.

- **Turning Mode**  
  Propulsion combined with fixed steering deflection.

- **Experimental Mode**  
  Adjustable timing and angle parameters for testing.

---

## Engineering Design Considerations

Key control design considerations include:

- Simplicity and robustness
- Low computational complexity
- Ease of parameter tuning
- Compatibility with future sensor feedback

---

## Limitations and Future Extensions

Current limitations:

- Lack of closed-loop feedback
- Sensitivity to external disturbances

Future improvements may include:

- Integration of IMU or pressure sensors
- Heading stabilization using feedback control
- Adaptive propulsion frequency control
- Autonomous behavior implementation

---

---

# 控制系统架构说明（中文版）

## 总体概述

控制系统负责协调推进、转向以及运动节律，
实现仿生水母水下机器人的稳定可控运动。

系统采用**基于时间的开环控制架构**，
适用于原型验证与实验研究阶段。

---

## 系统组成

控制系统主要包括：

- 微控制器（MCU）
- 推进与转向执行器
- 电源与能量管理模块
- 预留的传感器接口

---

## 控制策略

### 脉冲式推进控制

推进系统采用周期性脉冲控制方式。

每个推进周期包含：

1. **收缩阶段**：腔体收缩，喷水产生推力  
2. **恢复阶段**：腔体回弹，完成补水  

控制器通过设定频率和占空比
精确控制推进节律。

---

### 转向控制耦合

转向控制通过调节导流机构偏转角度实现。

在推进过程中：

- 导流板居中 → 直线运动  
- 导流板偏转 → 转向运动  
- 连续调节 → 曲线运动  

转向控制与推进节律保持同步，
保证运动平稳性。

---

## 控制流程

系统控制流程如下：

1. 系统初始化  
2. 设置推进参数  
3. 设置转向角度  
4. 执行推进与转向循环  
5. 持续运行或停止  

---

## 时间与同步控制

稳定运动依赖精确的时间控制。

系统保证：

- 推进周期一致性  
- 推进与转向相位协调  
- 运动状态切换平滑  

---

## 控制模式

系统支持多种控制模式：

- **直行模式**  
- **转弯模式**  
- **实验调试模式**  

---

## 工程设计考虑

控制系统设计重点包括：

- 结构与逻辑简洁  
- 计算负担小  
- 参数易于调整  
- 便于后续扩展  

---

## 局限性与未来改进

当前系统局限：

- 缺乏闭环反馈  
- 抗扰动能力有限  

未来可扩展方向：

- 引入姿态与深度传感器  
- 闭环姿态控制  
- 自适应推进策略  
- 自主水下行为  
