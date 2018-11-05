# 调试经验
	by lada
> - https://github.com/ladadidadida/ganhacks
> - 关于 g 和 d训练次数的问题： 主要取决于学习率，而不取决于g和d的网络复杂程度。<br>需要分情况讨论，大部分开源代码采用的方案是多训练几次d ， 但是在传感器数据集上，多训练几次g更有效 。 
> - acgan 的辅助分类器在一定程度上反映了生成器生成图片质量的好坏，但是不能判断生成图片的类别是否是均衡的。<br>生成器生成的图像越假，这种假图对判别器+分类器的参数的影响就越大，会使得分类器并不能表现出很好的性能。
> - 在generator中，使用res block的结构能够生成质量更逼真的图片。
> - 在generator中，所有的norm方式的效果都是不如batch norm的，在generator中即便使用了spectral norm的形式，也是要使用batch norm的。batch norm对于generator的效果的收益是非常大的 。 
> - 在真实数据集输入判别器的时候在真是样本上叠加噪声是有利于生成优质样本的。