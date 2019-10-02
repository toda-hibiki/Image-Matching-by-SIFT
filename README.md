# Image-Matching-by-SIFT

Overview
-

SIFTによる画像間のマッチングを行います。2019年春より、特許が切れたので、更に使われることになると考えています。  
また、OpenCV3から、実行に、opencv-contribが必要になりました。
SIFTによるマッチングにRANSACを適用しています。  
RANSACを計算する際にホモグラフィ変換行列を求めているので、画像がどれだけ回転しているかの情報を得ることができます。　　

Environment
-

Python3.6  
OpenCV-python:3.4.2.17  
OpenCV-contrib-python:3.4.2.17  
*OpenCVとOpenCV-contribのバージョンは合わせる必要がある  
numpy  
matplotlib  

Procedure
-

1. 入力画像のインプット  
1. それぞれの画像に対して、特徴点を取得する  
1. 総当りマッチングで対応付けを行う  
1. しきい値による、信頼度の高い特徴点の選択  
1. RANSACによる対応付けの交差除去  
1. 結果の出力  



