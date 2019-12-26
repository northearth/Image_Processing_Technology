# 課題2レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，グレースケールに変換し，表示した結果（以下，グレースケール原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_0.jpg)  
図1 グレースケール原画像

グレースケール原画像を2階調の画像に変換するには，画像に含まれる階調を2種類に分割する必要がある．

グレースケール原画像は，256階調の画像であるから，階調が0以上127以下のものと128以上256以下であるものに分割すればよい．

IMG = ORG>128; %階調を2つに分割

2階調処理を行ったの結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_1.jpg)  
図2 2階調画像

同様にグレースケール原画像を4階調の画像に変換するには，画像に含まれる階調を4種類に分割すればよい．したがって，

IMG0 = ORG>64; %階調が65以上128以下のもの
IMG1 = ORG>128; %階調が129以上192以下のもの
IMG2 = ORG>192; %階調が193以上256以下のもの

ここで，分割した階調を一つの画像として結合する．すらわち，

IMG = IMG0 + IMG1 + IMG2;

とする．4階調処理を行ったの結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_2.jpg)  
図3 4階調画像

同様に，8階調の画像は以下の処理によって変換できる．

IMG00 = ORG>32; %階調が33以上64以下のもの

IMG01 = ORG>64; %階調が65以上96以下のもの　
IMG02 = ORG>96; %階調が97以上128以下のもの　
IMG03 = ORG>128; %階調が129以上160以下のもの　
IMG04 = ORG>160; %階調が161以上192以下のもの　
IMG05 = ORG>192; %階調が193以上224以下のもの　
IMG06 = ORG>224; %階調が225以上256以下のもの　
IMG = IMG00 + IMG01 + IMG02 + IMG03 + IMG04 + IMG05 + IMG06; %　画像の結合

8階調処理を行ったの結果を図4に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_3.jpg)  
図4 8階調画像

このように階調が増えていくと，被写体の凹凸や形状などがはっきりと区別できるようになることがわかる．
