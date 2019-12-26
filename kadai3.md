# 課題3レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_0.jpg)  
図1 白黒濃淡原画像

ここでは，輝度値を4パターン設定し，閾値処理を行う．

はじめに，輝度値64を閾値として閾値処理を行う．

IMG = ORG > 64; % 輝度値が64を超える画素を1，その他を0に変換

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_1.jpg)  
図2 閾値64での閾値処理画像

つぎに，輝度値96を閾値として閾値処理を行う．

IMG = ORG > 96; % 輝度値が96を超える画素を1，その他を0に変換

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_2.jpg)  
図3 閾値96での閾値処理画像

そして，輝度値128を閾値として閾値処理を行う．

IMG = ORG > 128; % 輝度値が128を超える画素を1，その他を0に変換

この結果を図4に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_3.jpg)  
図4 閾値128での閾値処理画像

最後に，輝度値192を閾値として閾値処理を行う．

IMG = ORG > 192; % 輝度値が192を超える画素を1，その他を0に変換

この結果を図5に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_4.jpg)  
図5 閾値192での閾値処理画像

白黒濃淡画像では，輝度値0を白，輝度値256を黒とし，その間を256等分に分割し濃淡を表現している．

上記処理から読み取れるように，閾値を変化させることで，画像内の白と黒の割合が変化していることがわかる．
