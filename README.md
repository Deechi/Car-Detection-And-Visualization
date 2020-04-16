# Car-Detection-And-Visualization
画像から車両を検出し可視化するアルゴリズム
## 概要
駐車場の空き状況をカメラで監視し、自動で管理できれば省人化・コストダウンにつながる。  
そこで、「背景差分法」を用いて画像から車両を検出しヒートマップで可視化するアルゴリズムを開発した。  
開発環境はJupyter Notebook  
使用したライブラリはOpenCV(バージョン3.4)
## データ
駐車場に設置したカメラで15分ごとに撮影した画像を用いる。  
  
<img src = "https://user-images.githubusercontent.com/63439267/79410632-f13b9280-7fdb-11ea-880c-8a5a6cadc6b3.jpg" width = "300" height = "180">
  
## 手法
背景差分法は照明変化に弱いというデメリットがある。  
今回は各画素値を正規化することで照明変化に頑健な手法を実装した。
  
<img src = "https://user-images.githubusercontent.com/63439267/79412123-aface680-7fdf-11ea-8c9e-46e8317caabd.PNG" width = "100" height = "30"> &emsp;
x &thinsp; : &thinsp; 各画素値 &emsp;
u &thinsp; : &thinsp; 全画素値の平均 &emsp;
std &thinsp; : &thinsp; 全画素値の標準偏差 &emsp;
# 結果
入力画像の駐車状況に応じたヒートマップが出力できていることが分かる。
<img src = "https://user-images.githubusercontent.com/63439267/79416334-5e562480-7fea-11ea-9b78-47e58f86df41.jpg" width = "300" height = "180"> &emsp; &rArr;
<img src = "https://user-images.githubusercontent.com/63439267/79416563-eb00e280-7fea-11ea-8b35-9ddda62c7880.jpg" width = "300" height = "180">

