# 課題7レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai7_0.jpg)  
図1 白黒濃淡原画像

ここでは，画素のダイナミックレンジを0から255に変更する．

まず，処理を行う前の濃淡白黒原画像のヒストグラムを図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai7_1.jpg)  
図2 白黒濃淡原画像のヒストグラム

ここから，ダイナミックレンジの変更を行う．

まず，輝度値を整数配列から倍精度配列に変換を行う．

ORG = double(ORG);  

次に，輝度値の最大値・最小値を算出し，ダイナミックレンジを変更する．

mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  

この結果を図3に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai7_2.jpg)  
図3 ダイナミックレンジを変更した白黒原画像

この画像に対して，輝度値を倍精度配列から8ビット符号なし整数への変換を行う．これは，関数imhist()が規定の設定で256個のビンを使用していることに起因する．

ORG = uint8(ORG);  

この処理の後，関数imhist()を用いて画素の濃度ヒストグラムを生成し，表示する．

imhist(ORG); % ヒストグラムの表示

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai4_1.jpg)  
図2 ダイナミックレンジを変更した白黒原画像のヒストグラム

なお，　前述の処理を行わずにヒストグラムを生成しようとしても表示することはできない．

今回の場合は，白黒濃淡原画像がもともと0から255の輝度値を持つ画像であったことから，処理の前後で変化は見られなかった．

輝度値が短い範囲に集中している画像を用いることで，変化がみられると考えられる．