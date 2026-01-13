# RTPC
RTPC: Deep Reinforcement Learning-based Trajectory Planning with Continuous Pose Representation for 6-DoF Free-floating Space Robot

## Requirement
Ubuntu 18.04 / CentOS 7.5

Python == 3.8

PyTorch == 1.13.1

NumPy == 1.24.3

PyBullet == 3.2.5

## 项目结构
- `Agents/`：强化学习算法实现与训练逻辑封装。
  - `PPO_continuous.py`：连续动作空间的 PPO 智能体实现，包含动作采样与更新逻辑。
  - `__init__.py`：包初始化文件。
- `Envs/`：基于 PyBullet 的仿真环境与对象封装。
  - `pybullet_SpaceManipulatorReacherMultiagent.py`：多智能体空间机械臂到达任务环境。
  - `objects.py`：UR5 机械臂与目标物体等仿真对象类。
  - `__init__.py`：包初始化文件。
- `Models/`：神经网络模型定义。
  - `PPO_actor_critic.py`：PPO 的 Actor/Critic 网络结构定义。
  - `__init__.py`：包初始化文件。
- `Utils/`：训练过程的通用工具与数据结构。
  - `normalization.py`：状态归一化与奖励缩放工具。
  - `replaybuffer.py`：PPO/Off-Policy 训练缓冲区实现。
  - `utils.py`：常用工具函数（目录管理、日志、评估等）。
  - `__init__.py`：包初始化文件。
- `meshes/`：仿真模型网格资源。
  - `mug/mug.STL`：杯子目标物体的网格模型。
  - `satellite/satellite.STL`：卫星本体网格模型。
- `urdf/`：仿真模型的 URDF 描述文件与许可。
  - `ur5.urdf`：UR5 机械臂 URDF。
  - `satellite.urdf`：卫星 URDF。
  - `mug.urdf`：目标物体 URDF。
  - `LICENSE`：URDF/模型相关许可信息。
- `RTPC.py`：训练与评估入口脚本。
- `README.md`：项目说明与使用文档。
- `LICENSE`：项目许可证。

## Trajectory Planning Training Process (6 Agents)
https://github.com/user-attachments/assets/0a07b9bf-303c-47c5-8a5a-58faa6005b97

## Trajectory Planning Evaluation Process
https://github.com/user-attachments/assets/fb6dfd9a-124d-4bcc-b44f-9d7f3668b134

