# 信号处理算法库
 
 本项目旨在追踪建立最先进的信号处理算法库。从算法理论原理，实现方法，到落地demo。
 目前是个人业余收集和整理，知识和精力都有限，欢迎有识之士参与贡献。
 欢迎大家任意`Fork`,`Star`,`watch`.
 demo一般来自网络共享开源的资源。或者自己根据论文原理实现。欢迎批评指正。
 如涉及侵权，请随时联系删除787452269@qq.com。
 
 > 声明：本算法库仅作学习交流之用。如未经许可用作其他商业用途，保留追责权利。

## 1.经典的传统方法
### 时域
时域特征计算相对简单，MATLAB都有非常多的库函数。也有人已经进行了总结。直接引用。源自知乎专栏。  
* [时域特征值提取的MATLAB代码实现（均方根、峰值因子、脉冲因子、裕度因子、峭度因子、波形因子和偏度等）](https://zhuanlan.zhihu.com/p/36162561)  
* [信号时域分析方法的理解（峰值因子、脉冲因子、裕度因子、峭度因子、波形因子和偏度等）](https://zhuanlan.zhihu.com/p/35362151)  
* [时域分析——无量纲特征值含义一网打尽](https://zhuanlan.zhihu.com/p/57445453)    
* [时域分析——有量纲特征值含义一网打尽](https://zhuanlan.zhihu.com/p/57153601)  
* [python实现信号时域统计特征提取](https://blog.csdn.net/qq_34705900/article/details/88389319)  
* [Envelope Detction for Signal Analysis](https://ww2.mathworks.cn/matlabcentral/fileexchange/37545-envelope-detction-for-signal-analysis?s_tid=FX_rc1_behav)

### 频域
* [信号频域分析方法的理解（频谱、能量谱、功率谱、倒频谱、小波分析）](https://zhuanlan.zhihu.com/p/34989414)
* [频域特征值提取的MATLAB代码实现（频谱、功率谱、倒频谱）](https://zhuanlan.zhihu.com/p/36163931)
* fft专题

### 滤波
* 无限长单位脉冲响应（Infinite impulse response,IIR）滤波器
  [Infinite impulse response](https://en.wikipedia.org/wiki/Infinite_impulse_response)  
  * [使用matlab设计IIR巴特沃斯低通滤波器](https://blog.csdn.net/Stynis/article/details/80531803)  
    [matlab buttord 函数](https://ww2.mathworks.cn/help/signal/ref/buttord.html?searchHighlight=buttord&s_tid=doc_srchtitle)  
  * [MATLAB|切比雪夫低通滤波器设计与滤波实现](https://www.jianshu.com/p/2a0d6d587bc3)  
    [matlab cheb1ord 函数](https://ww2.mathworks.cn/help/signal/ref/cheb1ord.html?s_tid=doc_ta) 
  
* 有限长单位脉冲响应（Finite impulse response,FIR）滤波器
  * [Finite impulse response](https://en.wikipedia.org/wiki/Finite_impulse_response)  
  
* [维纳滤波 Wiener filter](https://zh.wikipedia.org/wiki/%E7%BB%B4%E7%BA%B3%E6%BB%A4%E6%B3%A2)  
  由于后续算法变分模态分解中使用到。  
* [卡尔曼滤波 Kalman filter](https://zh.wikipedia.org/wiki/%E5%8D%A1%E5%B0%94%E6%9B%BC%E6%BB%A4%E6%B3%A2)  
 扩展的关于Vold-Kalman Order Filtering  附matlab分享的相关代码。用于转速跟踪是当前研究的热点。  
 [Vold-Kalman order tracking code](https://ww2.mathworks.cn/matlabcentral/fileexchange/32639-vold-kalman-order-tracking-code?s_tid=FX_rc1_behav)  
 [Second generation Vold-Kalman Order Filtering](https://ww2.mathworks.cn/matlabcentral/fileexchange/36277-second-generation-vold-kalman-order-filtering)  

  

关于数字滤波，相关详细原理，请参考 ：程佩青. 数字信号处理教程(第五版)[M]. 清华大学出版社, 2017.  

### 其他


## 2.信号自适应分解

* [经验模态分解EMD&EEMD及其扩展和改进](./doc/EMD.md)
* [变分模态分解(Variational Mode Decomposition,VMD)](./doc/VMD.md)
* [局部均值分解(local mean decomposition,LMD)](./doc/LMD.md)
* [自适应局部迭代滤波(Adaptive Local Iterative Filtering,ALIF)](./doc/ALIF.md)
* [非线性模态分解 Nonlinear Mode Decomposition.NMD](./doc/NMD.md)
* [固有时间尺度分解(Intrinsic time-scale decomposition,ITD)](./doc/ITD.md)
* [希尔伯特振动分解(Hilbert Vibration Decomposition,HVD)](./doc/HVD.md)
* [时变滤波经验模态分解Time varying filter based empirical mode,TVF-EMD](./doc/TVF_EMD.md)
* [奇异谱分解 (Singular Spectrum Decomposition,SSD)](./doc/SSD.md)
* [经验小波 (Empirical Wavelet Transforms,EWT)](./doc/EWT.md)
* [短时窄带模式分解 (short-time narrow-banded mode decomposition,STNBMD)](./doc/STNBMD.md)
* [spatio-spectral decomposition](https://github.com/svendaehne/matlab_SSD)
* 一些新的分解方法
  * 极值点加权模式分解EWMD
  * 极值点对称模式分解
  * 辛几何模式分解symplectic geometry mode decomposition
  * [群分解(Swarm-Decomposition,SwD)](./doc/SwD.md)
  * 原子分解

## 3.时频分析方法
* [TFAT 时频工具](./doc/TFA_Tools.md)
* STFT
* SST
* [Time-frequency ridge detection](./doc/TFRD.md)

## 3.冲击特征检测

* [最小熵反褶积](./MED.md)

## 4.时间序列熵分析
* [排列熵(Permutation Entropy,PE)](./doc/PE.md)
* [近似熵（Approxiamte Entropy，ApEn）](./doc/ApEn.md)
* [样本熵（Sample Entropy，SampEn)](./doc/SamEn.md)
* 条件熵（Conditional Entropy）
* 修正条件熵（Corrected Conditional Entropy）
* 模糊熵（Fuzzy Entropy，FuzzyEn)
* 香农熵（Shannon Entropy，SE）
* 能量熵
* 谱熵
* 色散熵Dispersion entropy (DispEn)

## 5.一些开源的信号处理综合算法资源
* [Python for signal processing](https://github.com/unpingco/Python-for-Signal-Processing)
* [Digital Signal Processing for Javascript](https://github.com/corbanbrook/dsp.js)
* [Numerical Tours of Signal Processing](https://github.com/gpeyre/numerical-tours)
* [Digital Signal Processing - Theory and Computational Examples ](https://github.com/spatialaudio/digital-signal-processing-lecture)
* [Signal Processing Tools for MATLAB](https://github.com/JacobD10/SoundZone_Tools)
* [Basic-Rotating-Machine-Vibration-Analysis](https://github.com/ZhaoZhibin/Basic-Rotating-Machine-Vibration-Analysis)

[:top:返回顶部](#信号处理算法库)


