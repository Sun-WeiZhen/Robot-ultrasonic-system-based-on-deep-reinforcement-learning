# Robot-ultrasonic-system-based-on-deep-reinforcement-learning
If you do not understand Chinese, please read the introduction below

Training robot ultrasonic system using deep reinforcement learning.Because ultrasound doctors mainly use discrete motion to control ultrasound probes, most current work is based on DQN. The essential learners we use are also DQN series algorithms, but we have improved the algorithms. Considering the individual differences of patients and the safety of patients, we completed the experiment in the simulation environment. In addition, we also set up the molding reward function and other methods to improve the sample efficiency.
Our project is implemented in python.
Use pytorch to build a network model.
Considering the large amount of image data, we use ResNet18 as the basic network framework of DQN.
We have proposed some molding reward functions, but the experimental results are not ideal, so we use the parameterized molding reward functions.

Our team includes four national ultrasound doctors from Jiangsu Provincial People's Hospital to analyze and decompose each standard organ plane's collection tasks and actions in detail. We hope to find a general control method.

We found that under the influence of individual differences of patients, the robot ultrasound system trained in the natural environment could not be transferred to other volunteers. Therefore, our subsequent suggestion is to train in the simulation environment, collect many video demonstration tracks, and use brute force-solving methods to train the robot ultrasonic system.
Our main idea is that the design of our movement space must be simple and symbolize the control rules of ultrasound doctors. We can not completely simulate the actions of ultrasound doctors. Because although the ultrasonic doctors' actions are discrete, they can rotate and translate the probe to any angle. This kind of action is beyond DQN's reach. However, experiments in the simulation environment found that our action space can almost meet the demand; the probe needs to take more steps.

The principle of designing the shaping reward function must align with the thinking of ultrasound doctors. Therefore, we design three shaping reward functions.

Our previous discussion work lasted for two years. We discussed the current work related to the conventional image-based and location-based visual servo, which is not general. So we turn our goal to deep intensive learning.

Data collection mainly includes demonstration data and a simulation environment.

This link has a clinician with a senior professional title who can help us anytime.
Regarding some technical guidance for in-depth intensive learning, we have two academician teams working on robots and computers for guidance,

For testing and training in the natural environment, we mainly need to solve the following problems:

At least, this is the difficulty our team encountered

First, the computer responsible for the ultrasonic system is independent, and we cannot deploy the ROS system on this computer.

Therefore, at this time, we have two computers, one for controlling the mechanical arm and the other for the robot ultrasonic system.

The two systems need to communicate and transmit ultrasonic images.

The communication mechanism is very complex, and we must ensure that the ultrasound images obtained at each step are correct through sufficient delay.

Setting delays and aligning timestamps are more complex than the high research training model.

Therefore, the training time will be very long under the actual system.

In addition, we need to deploy modules such as yolo5s algorithm to ROS, which is a relatively engineering work.
It is difficult for the robot ultrasonic system to build a simulation environment. We use the grid to build the simulation environment, so we need to do a lot of high-density image acquisition work.

Collecting expert demonstration data is relatively simple.



We find that if the simulation environment is poorly designed, the training algorithm is generally nonconvergent. Therefore, it took us nearly half a year to build the simulation environment. The main work is wasted on image acquisition and training.

In my four years of doctoral career, two years of detailed analysis, and one year of experimental preparation, until now, I have achieved some works.



如果你是中国人，就看这里吧
我们的团队包括江苏省人民医院4位国家级超声科医生来详细分析和分解每个器官标准平面的采集任务和动作，我们希望发现一个具有一般性的控制方法。
我们发现受到患者个体差异性的影响，在真实环境下训练出来的机器人超声系统根本无法迁移到其他志愿者身上。因此，我们后续的建议是在仿真环境下训练，采集大量的视频演示轨迹，使用暴力求解的方法来训练机器人超声系统。
我们的主要思想是我们的动作空间的设计一定要简单并且符号超声科医生的控制规则。事实上我们根本无法完全的模拟超声科医生的动作。因为，虽然超声科医生的动作虽然是离散的，但是他们可以将探头向任何角度旋转和平移。这种动作对于DQN来讲只能是望尘莫及。但是，在仿真环境下的实验发现，我们的动作空间也差不多可以满足需求，就是探头需要走更多的步骤。
我们设计塑型奖励函数的原则是一定要符合超声科医生的思维。因此，我们设计了三个塑形奖励函数。
我们的前期讨论工作足足有两年之久，我们讨论了现在的常规的基于图像的视觉伺服和基于位置的视觉伺服的相关工作，这些工作不具有一般性。所以我们将目标转向深度强化学习。
关于数据采集，主要包括演示数据和仿真环境。
在该环节，我们有1个具有高级职称的超声检查临床医生帮助，他可以随时给我们提供帮助。

我们的项目是使用python语言实现的
使用pytorch搭建网络模型
考虑到图像数据量较大，我们使用ResNet18作为DQN的基础网络框架。
我们提出了一些塑型奖励函数，但是实验效果并不理想，因此我们使用了参数化的塑型奖励函数。

关于深度强化学习的一些技术性的指导，我们有两个与机器人和计算机相关的研究工作的院士团队作指导，
关于在在实际环境中测试和训练，我们主要需要解决下面的一些问题：
至少我们团队遇到的困难是这样的
首先，负责超声系统的计算机是独立的，我们无法在该计算机上部署ROS系统。
因此，此时我们有两个计算机，一个用于控制机械臂，一个用于机器人超声系统。
这两个系统之间需要通信并传递超声图像。
通信机制很复杂，我们需要通过足够的延迟来保证每个时间步得到的超声图像是正确。
设置延迟和将时间戳对齐其实比高科研训练模型还复杂。
因此，在实际系统下训练时间会很长。
此外，我们需要将yolo5s算法等模块部署道ROS，这都是一些比较工程性的工作。

对于机器人超声系统来讲，搭建仿真环境真的很困难。我们使用网格的方式搭建仿真环境，因此我们需要进行大量高密度的图像采集工作。
采集专家演示数据则相对简单。

我们发现如果仿真环境设计的不好，训练算法一般都是不收敛的。因此，就搭建仿真环境这块，我们花了将近半年的时间。其中主要工作浪费在采集图像和训练上了。
我四年的博士，两年的详细分析和一年的实验准备，直到现在才有了一些成果。






