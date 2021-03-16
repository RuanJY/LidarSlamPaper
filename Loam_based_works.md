# 基于LOAM的激光雷达SLAM
这些工作主要围绕着原版本的几个不足展开：没有回环，没有图优化，线性运动假设简单，松耦合IMU，特征提取简单，动态物体去除			

|主要改进|文章|发表|作者|主要内容|
|----|----|----|----|----|
|初始	|LOAM: Lidar Odometry and Mapping in Real-time	|RSS 2014	|Ji Zhang and Sanjiv Singh  |	基本，IMU松耦合|
|紧耦合|	Visual-lidar Odometry and Mapping: Low-drift, Robust, and Fast |ICRA 2015|Ji Zhang and Sanjiv Singh | 加视觉紧耦合|
|	|Laser–visual–inertial odometry and mapping with high robustness and low drift	|JFR 2017|Ji Zhang and Sanjiv Singh |加IMU紧耦合，分析了退化场景下的耦合方法|
|	|Tightly Coupled 3D Lidar Inertial Odometry and Mapping|ICRA 2019|Haoyang Ye1, Yuying Chen1 and Ming Liu1|紧耦合IMU，同时有局部图优化，在线标定外参，高动态场景有较大提升|
|	|LIC-Fusion: LiDAR-Inertial-Camera Odometry|IROS 2019 |	Xingxing Zuo∗, Patrick Genevayy, Woosik Leey, Yong Liu∗, and Guoquan Huangy|紧耦合IMU，视觉和激光，基于滤波框架MSCKF|
|	|R-LINS: A Robocentric Lidar-Inertial State Estimator for Robust and Efficient Navigation|ICRA 2020|Chao Qin, Haoyang Ye, Christian E. Pranata, Jun Han, Shuyang Zhang, and Ming Liu|ESKF 耦合IMU|
|	|Robust High Accuracy Visual-Inertial-Laser SLAM System|IROS 2019 |Zengyuan Wang1, Jianhua Zhang1, Shengyong Chen2, Conger Yuan1, Jingqian Zhang1 and Jianwei Zhang3|紧耦合视觉IMU，整合VINS和LOAM，也有回环|
|	|A Joint Optimization Approach of LiDAR-Camera Fusion for Accurate Dense 3D Reconstructions|IROS 2019|Weikun Zhen Yaoyu Hu Jingfeng Liu Sebastian Scherer|三维重建，紧耦合视觉，更加细致地处理了外参计算问题|
|特征提取|	"LeGO-LOAM: Lightweight and Ground-Optimized Lidar Odometry and Mapping on Variable Terrain"|IROS 2018|"Tixiao Shan and Brendan Englot"|地面划分从而滤除噪声特征点，在有植被时表现明显更加鲁棒，优化问题拆成两个部分计算，减少了迭代步数|
|	|"A Robust Laser-Inertial Odometry and Mapping Method for Large-Scale Highway Environments"|IROS 2019|"Shibo Zhao1, Zheng Fang1, HaoLai Li1, Sebastian Scherer2"|CNN去除动态车辆，基于ESKF耦合IMU，mapping使用NDT，解决高速路运动快、车辆多的场景|
|	|"Loam livox: A fast, robust, high-precision LiDAR odometry and mapping package for LiDARs of small FoV"|ICRA 2019|Jiarong Lin and Fu Zhang|解决小FOV雷达应用场景，在动态滤除，特征点，运动补偿上做了改进|
|	|"IN2LAMA: INertial Lidar Localisation And MApping"|ICRA 2019|"Cedric Le Gentil, Teresa Vidal-Calleja and Shoudong Huang"|离线，特征提取更加耐心细致，对IMU进行上采样，并且紧耦合，从而更好的去除畸变|
|闭环	|LLOAM: LiDAR Odometry and Mapping with Loopclosure Detection Based Correction	"|2019 IEEE International Conference on Mechatronics and Automationn|Xingliang Ji, Lin Zuo, Changhua Zhang, Yu Liu|加闭环|
|	|"Optimized LOAM Using Ground Plane Constraints and SegMatch-Based Loop Detection"|Sensors |"Xiao Liu 1,2, Lei Zhang 2, Shengran Qin 2,3, Daji Tian 2, Shihan Ouyang 2,3 and Chu Chen 1,2"|添加基于segmatch的闭环，和地面约束|
|	|"Trajectory Optimization of LiDAR SLAM Based on Local Pose Graph"|China Satellite Navigation Conference (CSNC) 2019 |Chunxu Chen|在LOAM后端加了位置图优化，效果有一定的提升|
	整理 by： 阮建源			
				
