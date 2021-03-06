**1** ** 引论 ** Introduction

Real-time monocular Simultaneous Localization and Mapping \(SLAM\) and 3D reconstruction have become increasingly popular research topics.

当下，实时单目~~即时~~同步定位和地图构建系统（SLAM）和三维空间环境重构~~俨然~~_已经_成为学术界流行的研究课题。

> **Note** Patrick交叉审稿: 范帝楷用“同步”比较贴切，localization和mapping两者的同步，蔡老师去掉“俨然”是合理的。我把have become翻译成“已经成为”，以上是我的拙见，请指教。

---

**当下，实时单目同步定位和地图构建系统(SLAM)和三维空间环境重构已经成为学术界流行的研究课题。**

---

Two major reasons are \(1\) their use in robotics, in particular to navigate unmanned aerial vehicles \(UAVs\) \[10, 8, 1\]，

**这里主要有两个原因：\(1\) 这些技术广泛使用在机器人领域，特别是用于无人飞行器（UAVs）\[10, 8, 1\]的自主导航中，**

and \(2\) augmented and virtual reality applications slowly making their way into the mass-market.

** \(2\) 还有，增强和虚拟现实技术的应用正逐渐进入大众市场。**

One of the major benefits of $$monocular$$ **SLAM** – and simultaneously one of the biggest challenges – comes with the inherent scale-ambiguity:

_单目_SLAM的主要优点之一，同时也是它的一个最大挑战之一，就是它固有的~~尺度歧义~~尺度不确定性（scale-ambiguity）这个问题：

> **Note** Patrick交叉审稿: 范帝楷用“尺度不确定性”在理解上比较直观。

---

_单目_ **SLAM的主要优点之一，同时也是它的一个最大挑战之一，就是它固有的尺度不确定性(scale-ambiguity)这个问题：**

---

The scale of the world cannot be observed and drifts over time, being one of the major error sources.

（SLAM对应的场景不同，尺度也不同，译者额外添加备注），场景的尺度，~~不容易~~_不能_被观测到，并且（单目SLAM计算过程中）随着时间（位姿估计）会产生漂移，这也是（单目SLAM）造成估计误差的主要原因之一。

> **Note** Patrick交叉审稿: 场景尺度不能被观测到

---

**(SLAM对应的场景不同，尺度也不同，译者额外添加备注)，场景的尺度，不能被观测到，并且(单目SLAM计算过程中)随着时间(位姿估计)会产生漂移，这也是(单目SLAM)造成估计误差的主要原因之一。**

---

The advantage is that this allows to seamlessly switch between differently scaled environments, such as a desk environment indoors and large-scale outdoor environments.

当然~~尺度歧义~~_尺度不确定性_的优点在于，可以对不同规模大小的空间环境之间走游切换，起到无缝连接的作用，比如从室内桌面上的（小）环境~~和到~~大规模的户外场景（等）。

---

**当然尺度不确定性的优点在于，可以对不同规模大小的空间环境之间走游切换，起到无缝连接的作用，比如从室内桌面上的(小)环境和大规模的户外场景(等)。**

---

Scaled sensors on the other hand, such as depth or stereo cameras, have a limited range at which they can provide reliable measurements and hence do not provide this flexibility.

**另一方面，诸如深度或**_**立体视觉**_**(双目)相机(stereo cameras)，这些具备深度信息的传感器(scaled sensors)，它们所提供的可靠深度信息范围，是有限制的，故而不能（像单目相机那样）具有尺度灵活性(flexibility)的特点。**

