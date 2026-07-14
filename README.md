# Literature Review Matrix for Master's Thesis

**Topic:** Optimized Digital Twin Architecture for Efficient Humanoid Bin Picking using Reinforcement Learning

| Paper | Dataset Used | Details |
|-------|--------------|---------|
| **Deep Learning for Robotic Bin Picking** | **RGB-D datasets**, **Dex-Net**, **YCB Object Dataset**, synthetic grasp datasets, and custom industrial RGB-D datasets | Most deep-learning bin-picking systems are trained using synthetic grasp data (e.g., **Dex-Net**) and evaluated on real robotic platforms using RGB-D cameras. Many studies also use the **YCB Object Dataset** for grasp planning and object recognition. Some industrial implementations collect their own RGB-D datasets to improve performance in specific production environments. |
| **Robotic Bin Picking: A Survey of Perception and Manipulation** | **No single dataset (Survey Paper)** | This paper is a literature survey and does **not** introduce or train on a dataset. Instead, it reviews the most widely used robotic bin-picking datasets, including **Dex-Net**, **YCB Object Dataset**, **LINEMOD**, **ROBI (Reflective Objects in Bin Picking)**, and several proprietary industrial datasets, comparing their applications, strengths, and limitations. |






















This table summarizes key papers relevant to the proposed research.

| Category | Paper | Problem Statement | Proposed Solution | Key Results | Limitations / Drawbacks | Relevance to This Thesis |
|----------|-------|-------------------|-------------------|-------------|-------------------------|--------------------------|
| Digital Twin + RL | Digital Twin-Empowered Robotic Arm Manipulation with Reinforcement Learning: A Comprehensive Survey (2026) | Lack of a unified overview of digital twins and RL for robotic manipulation. | Reviews digital twin architectures, RL algorithms, Sim2Real methods, and industrial applications. | Identifies research trends and open challenges. | Survey only; no experimental validation. Limited focus on humanoids. | Provides background and identifies research gaps your thesis addresses. |
| Digital Twin + RL | A Framework for Generating Synthetic Expert Demonstrations in Digital Twin-Based Robot Learning (2025) | Expert demonstrations for robot learning are expensive to collect. | Generates demonstrations automatically using a digital twin. | Improves learning efficiency while reducing manual data collection. | Focuses on imitation learning rather than RL optimization. | Useful for data generation and simulation workflow. |
| Sim2Real | Sim-to-Real Transfer in Deep Reinforcement Learning for Robotics: A Survey | RL policies often fail after deployment due to the reality gap. | Reviews domain randomization, adaptation, calibration, and fine-tuning methods. | Comprehensive taxonomy of Sim2Real techniques. | No new algorithm proposed. | Essential reference for your Sim2Real section. |
| Sim2Real | Transferring Policy of Deep Reinforcement Learning from Simulation to Reality (Nature Machine Intelligence) | Policies trained in simulation degrade on real robots. | Reviews practical transfer strategies and deployment techniques. | Highlights successful transfer methods. | Limited discussion of humanoid robots. | Strong justification for your deployment methodology. |
| Sim2Real | Reinforcement Learning in Robotic Systems: A Review on Sim-to-Real Transfer (2026) | Difficulties in transferring learned robot policies. | Reviews robust RL methods and transfer strategies. | Identifies current challenges and benchmarks. | Mostly review-based. | Supports your evaluation strategy. |
| Isaac Sim | Sim-to-Real Transfer for Mobile Robots using NVIDIA Isaac Sim (2025) | Mobile robot policies lack robust real-world performance. | Uses NVIDIA Isaac Sim with domain randomization for transfer. | Demonstrates successful zero-shot deployment. | Focuses on mobile robots, not manipulation. | Shows how Isaac Sim can support transfer learning. |
| Humanoid RL | Humanoid-Gym: Reinforcement Learning for Humanoid Robot with Zero-Shot Sim2Real Transfer | Humanoid locomotion and manipulation require efficient RL training. | RL training in Isaac Gym with zero-shot Sim2Real transfer. | High-quality humanoid control. | Primarily locomotion; limited industrial manipulation. | Useful reference for humanoid training. |
| Humanoid RL | Sim-to-Real Reinforcement Learning for Vision-Based Dexterous Manipulation on Humanoids | Dexterous manipulation is difficult to transfer from simulation. | Vision-based RL with Sim2Real deployment. | Strong manipulation performance. | Requires vision and dexterous hands. | Useful methodology for humanoid manipulation. |
| Humanoid RL | Crossing the Human-Robot Embodiment Gap with Sim-to-Real RL | Human demonstrations do not directly transfer to humanoid robots. | Learns embodiment-aware policies. | Better generalization across embodiments. | Computationally expensive. | Relevant to humanoid adaptation. |
| Humanoid Control | Survey on Learning-Based Whole-Body Control for Humanoid Robots (2026) | Whole-body control remains difficult due to high DoF. | Reviews learning-based controllers. | Identifies future research directions. | Survey only. | Supports your discussion of humanoid motion planning. |
| Robotic Manipulation | Reinforcement Learning for Pick-and-Place Operations in Robotics | Traditional pick-and-place lacks adaptability. | Reviews RL algorithms for robotic manipulation. | Summarizes PPO, SAC, DDPG, TD3. | Limited focus on humanoids. | Strong background for RL algorithms. |
| Robotic Manipulation | Survey on Deep Reinforcement Learning Algorithms for Robotic Manipulation | Many RL methods exist with varying performance. | Compares state-of-the-art RL methods. | Provides algorithm comparison. | Does not address industrial deployment. | Helps justify algorithm selection (PPO/SAC). |
| Dexterous Manipulation | Learning Dexterity from Simulation (OpenAI) | Dexterous robotic manipulation is difficult to learn directly on hardware. | Large-scale simulation with domain randomization. | Successful Sim2Real transfer. | Extremely high computational cost. | Demonstrates scalable RL training. |
| Robotic Grasping | QT-Opt: Scalable Deep RL for Vision-Based Robotic Manipulation | Robot grasping requires large datasets. | Large-scale off-policy RL. | Excellent grasp success rates. | High data requirements. | Reference for grasp optimization. |
| Robotic Grasping | Deep Reinforcement Learning for Robotic Grasping | Existing grasp planners are limited in dynamic environments. | RL-based grasp policy learning. | Improved grasp robustness. | Limited industrial validation. | Supports grasp strategy discussion. |
| Bin Picking | Deep Learning for Robotic Bin Picking | Reliable bin picking remains challenging. | Deep learning for grasp detection. | Improved object detection. | Does not optimize cycle time. | Highlights the need for efficiency-focused research. |
| Bin Picking | Robotic Bin Picking: A Survey of Perception and Manipulation | Comprehensive review of robotic bin picking. | Reviews perception, grasping, and manipulation methods. | Identifies open research gaps. | Mostly focuses on robotic arms. | Excellent literature review reference. |
| Bin Picking | Industrial Bin Picking Using Reinforcement Learning | Traditional planners struggle in cluttered environments. | RL-based manipulation. | Higher grasp success. | Focuses on robotic arms. | Closest application to your work. |
| Digital Twins | AI-Enhanced Digital Twin Systems for Warehouse Logistics Optimization (2026) | Warehouse systems require real-time optimization. | AI-enabled digital twins. | Improved operational efficiency. | Warehouse focus rather than manipulation. | Useful industrial motivation. |
| Motion Planning | MoveIt2 Motion Planning Framework | Complex motion planning for robots. | Modular ROS2 motion-planning framework. | Reliable collision-free planning. | Traditional planning; no learning. | Core component of your implementation. |
| Robot Control | ROS2 Control Framework | Hardware integration is complex. | Standardized robot controllers. | Stable deployment architecture. | Not an AI solution. | Required for real robot deployment. |
| Multi-Agent RL | Multi-Agent Reinforcement Learning: Foundations and Modern Approaches | Coordinating multiple agents is difficult. | Reviews MARL algorithms. | Comprehensive overview. | General rather than robotics-specific. | Supports your multi-agent RL objective. |
| Multi-Agent Robotics | Cooperative Multi-Agent Reinforcement Learning for Robot Manipulation | Robots need coordinated manipulation. | Cooperative RL policies. | Better collaboration between agents. | Increased computational complexity. | Relevant if comparing single- and multi-agent RL. |
| RL Algorithms | Proximal Policy Optimization (PPO) | Stable policy optimization is difficult. | PPO with clipped objective. | Stable and widely adopted RL algorithm. | Sample inefficient compared with some off-policy methods. | One of the primary algorithms proposed in this thesis. |
| RL Algorithms | Soft Actor-Critic (SAC) | Efficient continuous-control learning. | Maximum-entropy actor-critic framework. | High sample efficiency and robust performance. | More hyperparameters to tune. | One of the primary algorithms proposed in this thesis. |

## Identified Research Gap

1. Most studies focus on industrial robotic arms rather than humanoid robots.
2. Existing work emphasizes grasp success more than cycle-time optimization.
3. Few papers integrate Digital Twins, Reinforcement Learning, ROS2, MoveIt2, and Sim2Real into one framework.
4. Multi-Agent Reinforcement Learning for humanoid bin picking remains underexplored.
5. Reliable Sim2Real transfer for high-DoF humanoid robots is still an open research problem.
6. Industrial validation using NVIDIA Isaac Sim and humanoid robots is limited.

These gaps directly motivate the proposed master's thesis.
