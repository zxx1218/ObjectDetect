# 基于区域卷积神经网络的目标检测模型

1. 目前机器学习的替代者深度学习（卷积神经网络）发展迅速，在当下，无论是人脸识别，还是工业上的产品流水线检测，都逃脱不开目标检测的模型的应用，设计一个基于目标检测算法的xxx检测系统，用于本科毕业论文可以说是非常合适的，这篇github记录的就是一篇本科毕业设计所用到的模型算法，训练这个代码（**在RTX4090上大概只需要8个小时**），你只需要提供你想检测的物品（任何你想检测的物品），都可以得到一个目标检测模型，调用该模型即可实现对电脑自动识别目标的目的，**如果你有摄像头，你可以通过训练得到的模型去调用摄像头，通过摄像头动态监测（比如说监测是否有人经过或者是是不是有狗或者猫咪路过，也可以去检测单张图片，也可以把一段.mp4结尾的视频丢给模型。这个模型会给你返回用框框标记好的图片或者是视频）**

2. 训练上述代码，你需要拥有一块独立显卡（我非常不建议你使用没有显卡的电脑【即通过CPU训练】，因为CPU训练神经网络的速度只有显卡的1/100，在RTX4090下需要8小时，那通过CPU你估计要训练一两周）
3. 作者目前是**某TOP3计算机硕士在读**，方向就是人工智能，我可以帮忙训练模型，并提供给你源代码和训练后的模型并教给你怎么使用，或者提供远程部署服务，你只需要告诉我你的需求并提供给我图片数据集即可，我的收费很低，帮忙定制训练一个你想要的模型只需要**RMB 100元**。

### 作者联系方式：VX：Accddvva	QQ：1144968929

## 训练好的模型展示！

- **以下的所有图片，是我在公开的上千万张图的数据集中训练了19个小时的模型，目的只是为了展示效果**

### 相册里一张和朋友们的照片（每个锚框代表是一种类别的物品）



### 前两天在一家西餐厅随手拍的一张照片



### girl！（如果你想根据人脸识别具体是谁，只需要在图片里把这个人的名字标记上去就可以实现）



### 模型检测视频：记录同学的第一次台球体验（可以看到，视频的的每一帧都被模型添加了检测）

- 由于Github目前还不能在Readme中放视频，因此我把视屏上传到了bilibili，连接如下：

### 调用模型的时候控制台（CMD）的输出

- 可以看到目前调用的显卡是RTX4090，**这并不意味着没有显卡就不行，只是说有显卡可能一张图片只需要2-3毫秒，但如果通过CPU训练大概每张图需要15毫秒左右**

