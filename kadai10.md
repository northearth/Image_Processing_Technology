# 課題10レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_0.jpg)  
図1 白黒濃淡原画像

ここでは，エッジ抽出を体験する．

最初に，プレウィット法を用いてエッジ抽出を行う．

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_1.jpg)  
図2 プレウィット法を用いたエッジ抽出処理画像

次に，ソベル法を用いてエッジ抽出を行う．

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_2.jpg)  
図3 ソベル法を用いたエッジ抽出処理画像

最後に，キャニー法を用いてエッジ抽出を行う．

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

この結果を図4に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_3.jpg)  
図4 キャニー法を用いたエッジ抽出処理画像

このように，様々な方法を用いて画像のエッジ抽出を行うことができることがわかる．