# Robot-ultrasound-system-based-on-deep-reinforcement-learning
![image](https://user-images.githubusercontent.com/37693363/192133971-92744b00-171b-45be-a6cb-d962b40cf775.png)




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

Sorry, we are not very willing to provide the simulation environment. After all, we spent much time establishing the simulation environment. We will not release the simulation environment data until all our work is done.

??????????????????????????????????????????

??????????????????????????????????????????4???????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

??????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

?????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????DQN????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

???????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????
???????????????????????????????????????????????????????????????

????????????????????????1????????????????????????????????????????????????????????????????????????????????????????????????

????????????????????????python??????????????????

??????pytorch?????????????????????

?????????????????????????????????????????????ResNet18??????DQN????????????????????????

?????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

?????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????
?????????????????????????????????????????????????????????????????????????????????????????????
????????????????????????????????????????????????
??????????????????????????????????????????????????????????????????????????????????????????ROS?????????
????????????????????????????????????????????????????????????????????????????????????????????????????????????
?????????????????????????????????????????????????????????
??????????????????????????????????????????????????????????????????????????????????????????????????????????????????
???????????????????????????????????????????????????????????????????????????
???????????????????????????????????????????????????
????????????????????????yolo5s????????????????????????ROS?????????????????????????????????????????????

???????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????
??????????????????????????????????????????

???????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????
?????????????????????????????????????????????????????????????????????????????????????????????????????????

??????????????????????????????????????????????????????????????????????????????????????????
????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????




