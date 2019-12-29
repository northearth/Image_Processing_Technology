# 課題9レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_0.jpg)  
図1 白黒濃淡原画像

ここでは，メディアンフィルターを適用し，ノイズ除去を体験する．

最初に，関数imnoise()を用いて白黒濃淡原画像にノイズを添付する．

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_1.jpg)  
図2 ノイズを添付した画像

ここからは，フィルタを用いて添付したノイズを除去する．

まず，平滑化フィルタを用いてノイズ除去を行う．

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_2.jpg)  
図3 平滑化フィルタを用いてノイズ除去を行った画像

次に，メディアンフィルタを用いてノイズ除去を行う．

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_3.jpg)  
図3 メディアンフィルタを用いてノイズ除去を行った画像

最後に，作成したフィルタを用いてノイズ除去を行う．ここでは，以下の行列fを用いる．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_matrix.gif)  

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  

この結果を図4に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_4.jpg)  
図4 メディアンフィルタを用いてノイズ除去を行った画像