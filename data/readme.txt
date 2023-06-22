本压缩包中存放的代码Label_Extract，内容为标签提取
原本的人脸数据中，共有五个标签：性别、年龄、人种、表情、特殊特征，Label_Extract将前四个标签转换为DataFrame格式，而特殊特征在Label_Extract中没有提取。
鉴于组员所需，只将性别、年龄标签提取为可直接用于分类的ndarray格式并导出为npy文件。
若需要其他标签，可按照代码逻辑，将所需要标签从DataFrame中提取出来并转换成ndarray格式，便能用于分类。

npy文件说明

1.特征提取后的数据集
dlib库128维特征向量数据集：
trainDistance	训练集
testDistance	测试集

PCA特征降维数据集：
trainPCA	训练集
testPCA	测试集

LBP图像直方图特征数据集：
trainLBP	训练集
testLBP	测试集

LBP图像PCA降维数据集：
trainLBP_PCA	训练集
testLBP_PCA	测试集

2.标签，DR属于训练集，DS为属于测试集
DR_sex，DS_sex	性别标签，female与male
DR_sex_map, DS_sex_map	数值化后的性别标签，female = 0，male = 1
DR_age，DS_age	性别标签，child, teen, adult, senior
DR_sex_map, DS_sex_map	数值化后的年龄标签，child = 0, teen = 1, adult = 2, senior = 3

3.数据数量
DR_sex：male      1148	female     847
DS_sex：male      1277	female     719

DR_age：child      244	teen       261	adult     1436	senior      54
DS_age：child       68	teen        83	adult     1730	senior     115
	