##### 医学领域显微去高光研究

1. Li, R., Pan, J., Si, Y., Yan, B., Hu, Y. and Qin, H., 2019. Specular reflections removal for endoscopic image sequences with adaptive-RPCA decomposition. *IEEE transactions on medical imaging*, *39*(2), pp.328-340.

   

   提出 adaptive Robust Principal Component Analysis (Adaptive-RPCA，自适应主成分分析)：基于像素自适应检测高光图像，自动测量稀疏结果与高亮图像的相似距离，然后进行融合。RPCA分解方法是最有效和最流行的去除内窥镜图像高光的方法。

   ![Adaptive-RPCA](Images/Hightlight01.png)

2. Gao, Y., Yang, J., Ma, S., Ai, D., Lin, T., Tang, S. and Wang, Y., 2017. Dynamic searching and classification for highlight removal on endoscopic image. *Procedia Computer Science*, *107*, pp.762-767.

   

   基于SVM（支持向量机）的镜面分离方法；动态扩展，依据搜索策略和图像融合去除高光（人工生成Seed）。

3. Stehle, T., 2006. Removal of specular reflections in endoscopic images. *Acta Polytechnica*, *46*(4).

   

   将RGB转到YUC色彩空间，进行高光部分分割；光谱反卷积的方法去除高光

4. Ali, S., Zhou, F., Bailey, A., Braden, B., East, J.E., Lu, X. and Rittscher, J., 2021. A deep learning framework for quality assessment and restoration in video endoscopy. *Medical Image Analysis*, *68*, p.101900.

   旨在解决由于照明和器官的拓扑结构的可变性而导致的图像区域的过度曝光和曝光不足，目前常用方式包括SVM，encoder-decoder。机器学习框架包括Faster R-CNN， RetinaNet, YoloV3。提出了一种全自动、系统和全面的检测、分割以及恢复框架，分割基于YoloV3 特征金字塔架构，利用GAN进行恢复。

   ![Sequential process](Images/Hightlight02.png)

5. Fu, G., Zhang, Q., Zhu, L., Li, P. and Xiao, C., 2021. A Multi-Task Network for Joint Specular Highlight Detection and Removal. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition* (pp. 7752-7761).

   ![Multi Task 去高光](Images/Hightlight04.png)

6. Münzer, B., Schoeffmann, K. and Böszörmenyi, L., 2018. Content-based processing and analysis of endoscopic images and videos: A survey. *Multimedia Tools and Applications*, *77*(1), pp.1323-1362.

   ![内窥镜视频的分析](Images/Hightlight05.png)

   去高光方式：高光检测，反射像素“校正”（空间插值：利用内插像素代替高光；时间插值：考虑时间上下文，复杂适用性较差）。

7. Ghosh, A., Arnold, M., Ameling, S., & Lacey, G. (2010). Automatic segmentation and inpainting of specular highlights for endoscopic imaging. Eurasip Journal on Image and Video Processing, 2010. https://doi.org/10.1155/2010/814319

   色彩平衡自适应确定高光阈值，区分高光位置；利用高斯滤波后的图片修复图片

   ![Result](Images/Hightlight06.png)

8. Karapetyan, G., & Sarukhanyan, H. (2013). Automatic detection and concealment of specular reflections for endoscopic images. CSIT 2013 - 9th International Conference on Computer Science and Information Technologies, Revised Selected Papers. https://doi.org/10.1109/CSITechnol.2013.6710353

   YUV色度空间滑动窗分割高光部分；the modification frequency selective extrapolation (FSE) 算法隐藏高光错位。

9. Shen, D. F., Guo, J. J., Lin, G. S., & Lin, J. Y. (2020). Content-aware specular reflection suppression based on adaptive image inpainting and neural network for endoscopic images. Computer Methods and Programs in Biomedicine, 192, 105414. https://doi.org/10.1016/j.cmpb.2020.105414

   常用修复手法：隐藏、插值、相邻帧，本文中利用神经网络进行区域分类，修复手段为隐藏高光区域

   ![Process](Images/Hightlight07.png)

10. Liu, T., Chang, J., Wang, C., & Yang, L. (2021). Specular Reflections Detection and Removal Based on Deep Neural Network for Endoscope Images Specular Reflection Detection and Removal Based on Deep Neural Network for Endoscope Images. 10–12. https://doi.org/10.36227/techrxiv.16918234.v1

    利用全连接神经网络对高光像素进行提取，利用颜色映射方式修复图片

11. Monkam, P., Wu, J., Lu, W., Shan, W., Chen, H., & Zhai, Y. (2021). EasySpec: Automatic Specular Reflection Detection and Suppression from Endoscopic Images. IEEE Transactions on Computational Imaging, 7, 1031–1043. https://doi.org/10.1109/TCI.2021.3112117

    检测阶段：scaled-UNet （弱监督以及迁移学习，轻量化的U-net），利用CNN训练弱标记数据，然后利用少量精标注数据进行微调，利用迁移学习方式训练Scaled-UNet

    ![过程](Images/Hightlight08.png)

    高光修复设计GatedResUnet：基于Unet框架以及resNet，加入了context encoding block(CEB)

    ![修复](Images\HightLight09.png)

12. Yu, B., Chen, W., Zhong, Q., & Zhang, H. (2021). Specular Highlight Detection Based on Color Distribution for Endoscopic Images. Frontiers in Physics, 8(January), 1–7. https://doi.org/10.3389/fphy.2020.616930

​        通过自适应 R channel 与 B/G channel的差异阈值进行高光检测。

