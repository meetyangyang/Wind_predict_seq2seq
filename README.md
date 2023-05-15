# Wind_predict_seq2seq
基于seq2seq模型的风功率预测<br>

# 版本要求
python3.6<br>
tensorflow>=0.1 & <=1.15<br><br>
# 网络说明
1.利用简单神经网络将缺失数据补全<br>
2.基于seq2seq模型训练数据<br>
seq2seq模型示意图<br>
![](https://github.com/LeslieZhoa/Wind_predict_seq2seq/blob/master/img/1.png)

# 文件说明
## 数据 data/
2015年5,6月数据具体完整版.xlsx:原始风功率数据<br>
fitt.h5:剔除缺损数据，分好x,y<br>
twomonthes.h5:重载补全数据神经网络补全数据<br>
tdata1.h5:分好序列的数据文件<br>
## 程序
data.ipynb：数据处理代码相关说明(其中重载路径需重新定义)<br>
fitted.ipynb:补全数据网络的训练<br>
untitled0.py：重载补全数据网络代码脚本<br>
wind.ipynb:风功率预测训练代码<br><br>
# 结果显示
准确率采取1-均方根误差，其中验证集最好准确率为94%，可视化预测值与真实值曲线如下：<br>
![](https://github.com/LeslieZhoa/Wind_predict_seq2seq/blob/master/img/show.png)
# 参考文献 Reference

* [Yang, Y., Lang, J., Wu, J., Zhang, Y., Su, L., & Song, X. (2022). Wind speed forecasting with correlation network pruning and augmentation: A two-phase deep learning method. Renewable Energy, 198, 267-282.](https://www.sciencedirect.com/science/article/pii/S0960148122011351)
* [Sutskever, I., Vinyals, O., & Le, Q. V. (2014). Sequence to sequence learning with neural networks. Advances in neural information processing systems, 27.](https://proceedings.neurips.cc/paper_files/paper/2014/hash/a14ac55a4f27472c5d894ec1c3c743d2-Abstract.html)
