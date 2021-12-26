# The-Simpsons-Characters-Recognition
* THE SIMPSONS CHARACTERS RECOGNITION 

## File description
requirement.txt  程式所需安裝套件\
machine_learning_part_2.ipynb / machine_learning_part_2.ip  為程式碼\
machine_learning_part_2.sh  是測試和訓練腳本\
predict2.csv  預測結果\
110618019 甘鼎永 classification.pptx 報告
## Environment
colab\
Python                          3.6\
tensorflow                    2.7.0\
pandas                        1.1.5\
numpy                         1.19.5\
matplotlib                    3.2.2\
keras                         2.7.0\
sklearn                       0.0
## Program flow
### 1.Import API
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202021-12-27%20000105.png)

### 2.Attach Google Drive、Setting up variables
Setting image size(it can resize using Imagedatagen), test size , characters set, number of characters and data import
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%871.png)

### 3.Data processing
讀取google硬碟中辛普森照片資料並轉換成後續處理需要的格式
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%872.png)

Load data setting:將資料切分為訓練資料集與證資料集(85%vs.15%)，並對圖像的型別轉換與歸依會處理
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%873.png)

對資料訊息加強，有利於提升模型的精準度，將圖片以逆時針轉動、縮放幅度、水平翻轉來提高圖片的辨識度
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%874.png)

### 4.Model Building
建立Sequential 模型，設定卷積層與池化層的曾術與大小，加入 BatchNormalization 來加速模型收斂
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%875.png)

模型顯示
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%877.png)

為了提高訓練效率，當訓練成果收斂至一定程度時提前停止
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%876.png)

### 5.Model fit and Result
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%878.png)

視覺化模型結果:觀察 train and validation 的圖形，是否有overfitting 等問題
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%879.png)

### 6.Predict
讀取要測試的檔案並預測
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%8710.png)

### 7.Save file
存成csv檔，並把預測結果放入
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%8711.png)

### 8.Optimization
更改模型建置，像DenseNet121模型，因為原先使用的是基本的CNN模型，換一種模型可能可以提高預測結果
![](https://github.com/MachineLearningNTUT/classification-110618019KanTingYung/blob/main/photo/%E5%9C%96%E7%89%8712.png)


