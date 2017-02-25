**2 预备知识** Preliminaries

In this chapter we give a condensed summary of the relevant mathematical concepts and notation.

**在本章中，我们会简明扼要的给出（这篇论文）相关的数学定义和符号表示。**

In particular, we summarize the representation of 3D poses as elements of Lie-Algebras \(Sec. 2.1\),

**尤其在（2.1小节），我们会总结一下，三维空间位姿（如何）用李代数（ Lie-Algebras）的方式表达。**

derive direct image alignment as weighted least-squares minimization on Lie-manifolds \(Sec. 2.2\),

**然后（2.2小节）推导出图像直接配准法的实质，即：李群—流体（Lie-manifolds）上的加权最小二乘的最小化\(weighted least-squares minimization\)（优化问题）**

and briefly introduce propagation of uncertainty \(Sec. 2.3\).

**在（2.3小节）简要介绍（相机关键帧之间如何）传递（深度信息，即：深度的）不确定性的。**



**数学符号定义** Notation.

We denote matrices by bold, capital letters \(R\) and vectors as bold, lower case letters \(ξ\).

**“矩阵” 用粗体，大写字母表示，（比如：R）， ”向量” 用粗体，小写字母表示（比如：ξ）。**

The n’th row of a matrix is denoted by \[·\] n （$$$$$$[\cdot]_{n}$$） .

**矩阵的第n行用\[·\] n 来表示。**

Images I : Ω →R, （$$I: \Omega \rightarrow \mathbb{R}$$）

the per-pixel inverse depth map D : Ω → R +  （$$D: \Omega \rightarrow \mathbb{R}^{+}$$）

and the inverse depth variance map V : Ω → R + （$$V: \Omega \rightarrow \mathbb{R}^{+}$$） are written as functions, 

where Ω ⊂ R 2 is the set of normalized pixel coordinates, i.e., they include the intrinsic camera calibration.

**论文中提及的若干概念： 图像 I （Image），（像素级别的）逆深度图 D（简称逆深度图，per-pixel inverse depth map），逆深度方差图 V（inverse depth variance map），我们用数学映射关系的函数表达如下：**

**图像 I : Ω →R， （**$$I: \Omega \rightarrow \mathbb{R}$$**） （备注译者使用Latex符号表示）**

**逆深度图 D : Ω → R +  （**$$D: \Omega \rightarrow \mathbb{R}^{+}$$**）**

**逆深度方差图 V : Ω → R +  （**$$V: \Omega \rightarrow \mathbb{R}^{+}$$**）**

**其中：Ω ⊂ R 2 （**$$\Omega \subset \mathbb{R}^{2}$$**），Ω是归一化（normalized）的像素（二维）坐标点集合，即：包含相机内参（intrinsic）标定的参数。**

Throughout the paper we use d to denote the inverse of the depth z of a point, i.e., d = z −1 （$$d = z^{-1}$$） . \(这里是z的倒数，不是z-1\)

**在整篇论文中，三维空间中某一点的深度表示为z, 它的逆深度用d表示，两者的关系即：d = z −1 （**$$d = z^{-1}$$）。

