# 20181103
20181103报告

### 近期工作

> #### 论文阅读
>> - VAE & GAN：
>>> - Auto-Encoding Variational Bayes
>>> <br>Tutorial on Variational Autoencoders
>>> <br>见./blogs/VAE.md
>>> - Wasserstein auto-encoder
>>> <br>见./blogs/VAE.md
>> - 半监督 ：
>>> - semi-supervised learning with generative adversarial networks<br>在训练判别器(分类器)的时候，使用生成器生成的假样本来填充了原本类与类之间的间隔，以此来降低对抗样本被错误分类的几率，从而提高模型的泛化性能。

> #### 调试GAN模型
>> - 复现论文wgan_gp
>> - 复现论文wgan_sn： spectral norm 
>> - 将self attention应用在gan中
>> - 在generator中加入res block的结构，it works 。 
>> - 初步尝试VAE + GAN的形式，未仔细调整超参数，works 。
>> - 打分评价体系(half done)

> #### 调试经验
>> - 见ladasay.md

> #### 对比模型结果
>> - self attention <br>+ generator res_block batch norm <br>+ discriminator res_block spectral norm <br> 表现最好

### GAN的应用问题
> 目前搜集到的资料，GAN在CV方向的主要引用：
> - 分类（半监督）
> - 风格迁移
> - 语意分割
> - 图像生成（pix2pix）
> - 目标检测：
>> + A-Fast-RCNN: Hard positive generation via adversary for object detection
>> + Perceptual Generative Adversarial Networks for Small Object Detection

### 接下来工作
> - 细调vae + gan的代码细节 。 
> - 写wae代码，并将其与gan结合
> - 完善打分机制，在此基础下进一步对比模型。
> - 论文阅读：
>> - GAN相关 https://github.com/dongb5/GAN-Timeline & https://github.com/zhangqianhui/AdversarialNetsPapers
>> - GAN之外：ICLR CVPR 优秀的文章。搜集思路