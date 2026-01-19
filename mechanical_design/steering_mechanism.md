# Steering and Directional Control Mechanism

## Overview

In addition to forward propulsion, the biomimetic jellyfish-inspired underwater robot
requires the ability to adjust its movement direction.
Unlike conventional underwater robots that rely on differential propeller thrust,
this system achieves steering by **modifying the direction of the expelled water jet**.

Directional control is realized through a mechanically actuated flow-guiding structure
located at the water outlet.

---

## Steering Principle

The steering mechanism is based on the principle of **thrust vector deflection**.

By changing the orientation of the water jet relative to the robot body axis,
a lateral force component is introduced, resulting in a change in heading direction.

This approach preserves the simplicity and low-noise advantages of jet propulsion
while enabling directional maneuverability.

---

## Mechanical Structure

### Flow Deflector Design

A flow deflector (or guiding plate) is installed near the water outlet.
The deflector can rotate or tilt within a limited angular range.

Key components include:

- Flow deflector plate  
- Servo motor or micro-actuator  
- Rotational joint or hinge mechanism  
- Mechanical linkage for angle adjustment  

The deflector redirects the expelled water jet
without obstructing the intake process.

---

### Actuation Method

The deflector angle is controlled by a small actuator, such as:

- Servo motor  
- Stepper motor  
- Miniature DC motor with position feedback  

The actuator receives control commands from the onboard controller,
allowing real-time adjustment of the deflection angle.

---

## Steering Modes

The steering system supports multiple motion behaviors:

- **Straight Motion**  
  Deflector aligned with body axis, producing pure forward thrust.

- **Turning Motion**  
  Deflector angled to one side, generating asymmetric thrust.

- **Curved Trajectory**  
  Continuous partial deflection enables smooth turning paths.

- **Stationary Rotation (Optional)**  
  Alternating deflection patterns may induce rotational motion.

---

## Control Characteristics

Steering performance depends on:

- Deflection angle magnitude  
- Jet velocity during expulsion phase  
- Actuation response speed  

Small deflection angles produce gentle trajectory changes,
while larger angles result in sharper turns.

---

## Engineering Design Considerations

Key design trade-offs include:

- **Steering Authority vs. Efficiency**  
  Larger deflection angles increase turning capability
  but reduce forward thrust efficiency.

- **Mechanical Simplicity**  
  Limiting the number of moving parts improves reliability underwater.

- **Sealing and Waterproofing**  
  Actuator interfaces must be properly sealed to prevent water ingress.

---

## Advantages of Jet-Based Steering

Compared with differential propulsion steering,
the proposed mechanism offers:

- Reduced mechanical complexity  
- Lower acoustic signature  
- Improved robustness in cluttered environments  

---

## Limitations and Future Enhancements

Current limitations include:

- Limited steering torque at low jet velocities  
- Dependence on precise actuator control  

Potential future improvements:

- Adaptive deflection based on feedback sensors  
- Multi-directional nozzle designs  
- Integration with closed-loop heading control  

---

---

# 转向与方向控制机构设计说明（中文版）

## 总体概述

在实现前向推进的基础上，
仿生水母水下机器人还需要具备方向调整能力。
本系统不采用差速螺旋桨转向方式，
而是通过**改变喷水方向**实现转向控制。

该方式通过在出水口处引入导流结构，
实现对推进方向的控制。

---

## 转向基本原理

转向机构基于**推力矢量偏转原理**。

通过改变喷水方向相对于机器人轴线的角度，
在推进力中引入横向分量，
从而使机器人改变航向。

该方法在保持反冲喷射推进优势的同时，
实现了方向可控性。

---

## 机械结构设计

### 导流板结构

在喷水出口附近设置可调角度的导流板，
导流板可在一定角度范围内偏转。

主要组成包括：

- 导流板  
- 舵机或微型执行器  
- 转动铰链结构  
- 角度调节连杆  

导流板在不影响吸水过程的前提下，
对喷射水流进行方向引导。

---

### 驱动方式

导流板角度由执行器控制，例如：

- 舵机  
- 步进电机  
- 带位置反馈的小型直流电机  

执行器接收控制器指令，
实现导流角度的实时调整。

---

## 转向模式

系统可实现多种运动模式：

- **直线运动**：导流板与轴线对齐  
- **转弯运动**：导流板向一侧偏转  
- **曲线运动**：连续小角度偏转  
- **原地旋转（可选）**：交替偏转控制  

---

## 控制特性

转向性能主要受以下因素影响：

- 导流板偏转角度  
- 喷水阶段的喷射速度  
- 执行器响应速度  

小角度偏转可实现平滑转向，
大角度偏转可实现快速转向。

---

## 工程设计权衡

转向机构设计中重点考虑：

- **转向能力与推进效率之间的平衡**  
- **机械结构简化以提高可靠性**  
- **水密性与密封设计要求**  

---

## 喷射式转向优势

相较于差速推进方式，
该转向方法具有：

- 结构简单  
- 噪声低  
- 对水下复杂环境适应性强  

---

## 局限性与改进方向

目前转向系统的局限包括：

- 在低喷射速度下转向能力有限  
- 对执行器控制精度有一定要求  

未来可通过以下方向改进：

- 引入传感器反馈进行闭环控制  
- 多喷口或可变喷口结构  
- 转向与姿态联合控制策略  
