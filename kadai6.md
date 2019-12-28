# 課題6レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai6_0.jpg)  
図1 白黒濃淡原画像

今回は，2種類の方法によって二値化を行う．

まず，閾値を用いて二値化を行う．ここでは，閾値を128とする．

IMG = ORG>128; % 128による二値化  

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai6_1.jpg)  
図2 閾値128での二値化処理画像

つぎに，ディザ法を用いた処理により，二値化を行う．

IMG = dither(ORG); % ディザ法による二値化  

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai6_2.jpg)  
図3 ディザ法を用いた二値化処理画像

このように，画像の二値化は処理の方法によって結果が異なることがわかる．