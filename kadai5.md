# �ۑ�5���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai5_0.jpg)  
�}1 �����Z�W���摜

�����ŁC���ʕ��͖@��p���ĉ摜��l�����s���D

�܂��C��f�̔Z�x�q�X�g�O�����𐶐����C���̃f�[�^���x�N�g���Ɋi�[����D

H = imhist(ORG); %�q�X�g�O�����̃f�[�^���x�N�g��E�Ɋi�[  

���ɁC�v�Z�ɕK�v�ȕϐ����`����D

myu_T = mean(H); %H�̕��ϒl  
max_val = 0;  
max_thres = 1;  

�����āCFor���[�v��p���āC�����Z�W���摜�Ɋ܂܂��256�K�����Ƃɔ�����s���D

for i=1:255  
C1 = H(1:i); %�q�X�g�O������2�̃N���X�ɕ�����  
C2 = H(i+1:256);  
n1 = sum(C1); %��f���̎Z�o  
n2 = sum(C2);  
myu1 = mean(C1); %���ϒl�̎Z�o  
myu2 = mean(C2);  
sigma1 = var(C1); %���U�̎Z�o  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %�N���X�����U�̎Z�o  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %�N���X�ԕ��U�̎Z�o  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  

�Ō�ɁC����̌��ʂ���臒l���߁C�摜�̓�l�����s���D

IMG = ORG > max_thres;  

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai5_1.jpg)  
�}2 ���ʕ��͖@��p������l�������摜

���̂悤�ɁC�����Z�W���摜����C�摜�̓�l�����s�����Ƃ��ł����D