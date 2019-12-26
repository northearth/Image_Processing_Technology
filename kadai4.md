# 課題4レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai4_0.jpg)  
図1 白黒濃淡原画像

ここで，関数imhist()を用いて濃淡白黒原画像のヒストグラムを表示する．

imhist(ORG); % ヒストグラムの表示

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai4_1.jpg)  
図1 白黒濃淡原画像

ヒストグラムから読み取れるように，今回用いた白黒濃淡原画像では，

輝度値がおおよそ90から130までのものが多く含まれていることがわかる．