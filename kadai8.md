# 課題8レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai8_0.jpg)  
図1 白黒濃淡原画像

ここでは，二値化を行った画像の連結成分にラベルをつける．

まず，輝度値128を閾値として画像の二値化を行う．

IMG = ORG > 128; % 閾値128で二値化

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai8_1.jpg)  
図2 二値化を行った白黒濃淡原画像

ここで，関数bwlabeln()を用いて連結成分にラベル付けを行う．

IMG = bwlabeln(IMG); 

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai8_2.jpg)  
図3 ラベル付け処理を行った画像

このように，ラベル付けを行うことによって，二値化処理画像だけではわからない画像内の状態を視覚的に捉えることができる．