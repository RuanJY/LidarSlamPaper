Follow the conventional pipeline of SLAM, here are some paper utilizing semantic info.
# Creat info (Prediction)
This kind of methods predict (rather than extract directly) extra information from sensor data.
# Process info (Data Association)
Given info, the next problem is to determine the correspondence. Robust and efficient data association is the core issue in SLAM.
# Use info (Mapping)
This type of method focus on providing high-level map for advanced robotics applications.

| Type                |                        | Paper                                                                                 | Detial                       |
|---------------------|------------------------|---------------------------------------------------------------------------------------|------------------------------|
| Prediciton          | Depth                  | CNN-SVO                                                                               | 单双目深度估计                      |
|                     | Scale                  | Recovering stable scale in monocular SLAM using object-supplemented bundle adjustment | 尺度不确定性恢复                     |
|                     | Occlusion              | EmptyCities                                                                           | 对被遮挡的场景恢复后再做SLAM             |
|                     |                        | MBO                                                                                   | 去模糊网络                        |
| Data Association    | Learned Feature        | CNN-SLAM                                                                              | 用CNN网络进行特征匹配                 |
|                     |                        | AVP-SLAM                                                                              | 识别环境中的车道线等特征                 |
|                     |                        | CarFusion/OrcVIO                                                                      | 用到的结构化特征点LIFT/SuperPoint     |
|                     |                        | LodoNet                                                                               | 激光投影到2D平面提特侦匹配               |
|                     | Filter Noisy Info      | DynaSLAM                                                                              | 用MaskRCNN来做动态物体删除            |
|                     |                        | Suma++                                                                                | 动态滤除                         |
|                     |                        | SalientDSO                                                                            | 显著性应用                        |
|                     |                        | Lego_LOAM                                                                             | 滤除植物点                        |
|                     | Add Constrain          | PSF-LO                                                                                | 几何配准加语义约束                    |
|                     |                        | Probabilistic Data Association for Semantic SLAM                                      | 语义为隐含优化变量                    |
|                     |                        | Semantic-ICP                                                                          | 语义为隐含优化变量                    |
|                     |                        | Integrating Deep Semantic Segmentation Into 3-D Point Cloud Registration              | 语义filter                     |
|                     |                        | SIVO                                                                                  | 基于SVO，cubeslam物体级别           |
|                     | Deep Matching          | SuperGlue                                                                             | DL解决匹配问题                     |
|                     | Loop Closure/Long Term | X-View                                                                                | 长期回环检测                       |
|                     |                        | PointNetVLAD                                                                          | 激光回环                         |
|                     |                        |  Semantically Assisted Loop Closure in SLAM Using NDT Histograms                      | 含语义的直方图回环                    |
|                     |                        | GOSMatch                                                                              | 图匹配的回环                       |
| Solving             |                        | BA-Net                                                                                | DL方式做优化                      |
| Mapping             | With Tag               | Kimera                                                                                |  针对导航任务的SLAM算法结合，主要操作在Mesh上了 |
|                     | Object-level           |                                                                                       |                              |
|                     | Metric                 |                                                                                       |                              |
| End-to-End Odometry |                        | DeepVO                                                                                | 端到端的VO/SLAM                  |
