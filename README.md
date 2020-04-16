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
<img src = "https://user-images.githubusercontent.com/63439267/79412123-aface680-7fdf-11ea-8c9e-46e8317caabd.PNG" width = "100" height = "30">  
