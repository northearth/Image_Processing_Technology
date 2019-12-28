# 課題5レポート

画像「Yokohama_View.JPG」を原画像とする．この画像は縦1210画像，横1613画素による長方形のディジタルカラー画像である．

ORG=imread('Yokohama_View.JPG'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，白黒濃淡画像に変換し，表示した結果（以下，白黒濃淡原画像）を図1に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai5_0.jpg)  
図1 白黒濃淡原画像

ここで，判別分析法を用いて画像二値化を行う．

まず，画素の濃度ヒストグラムを生成し，そのデータを列ベクトルに格納する．

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納  

次に，計算に必要な変数を定義する．

myu_T = mean(H); %Hの平均値  
max_val = 0;  
max_thres = 1;  

そして，Forループを用いて，白黒濃淡原画像に含まれる256階調ごとに判定を行う．

for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  

最後に，判定の結果から閾値を定め，画像の二値化を行う．

IMG = ORG > max_thres;  

この結果を図2に示す．

![原画像](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai5_1.jpg)  
図2 判別分析法を用いた二値化処理画像

このように，白黒濃淡原画像から，画像の二値化を行うことができた．