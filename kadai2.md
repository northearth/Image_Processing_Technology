# 課題2レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_0.jpg)  
図1 白黒濃淡原画像

白黒濃淡原画像を2階調の画像に変換するには，画像に含まれる階調を輝度値に関して2種類に分類すればよい．

すなわち，白黒濃淡原画像は輝度値に関して256の階調を持つ画像であるから，輝度値が128を超えるものか，それ以外かに分類すればよい．

IMG = ORG>128; %階調を輝度値に関して2つに分類

2階調処理を行ったの結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_1.jpg)  
図2 2階調画像

同様に,白黒濃淡原画像を4階調の画像に変換するには，画像に含まれる階調を輝度値に関して4種類に分類すればよい．したがって，

IMG0 = ORG>64; %輝度値がが64を超え128以下のもの  
IMG1 = ORG>128; %輝度値が128を超え192以下のもの  
IMG2 = ORG>192; %輝度値が192を超えるもの 

ここで，分類した画像を一つの画像として結合する．すらわち，

IMG = IMG0 + IMG1 + IMG2;  

とする．4階調処理を行ったの結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_2.jpg)  
図3 4階調画像

また，8階調の画像は以下の処理によって変換できる．

IMG00 = ORG>32; %輝度値が32を超え64以下のもの  
IMG01 = ORG>64; %輝度値が64を超え96以下のもの  
IMG02 = ORG>96; %輝度値が96を超え128以下のもの  
IMG03 = ORG>128; %輝度値が128を超え160以下のもの  
IMG04 = ORG>160; %輝度値が160を超え192以下のもの  
IMG05 = ORG>192; %輝度値が192を超え224以下のもの  
IMG06 = ORG>224; %輝度値が224を超えるもの  
IMG = IMG00 + IMG01 + IMG02 + IMG03 + IMG04 + IMG05 + IMG06; %画像の結合  

8階調処理を行ったの結果を図4に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_3.jpg)  
図4 8階調画像

このように階調が増えていくと，被写体の凹凸や形状などがはっきりと区別できるようになることがわかる．
