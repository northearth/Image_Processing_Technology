# �ۑ�9���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_0.jpg)  
�}1 �����Z�W���摜

�����ł́C���f�B�A���t�B���^�[��K�p���C�m�C�Y������̌�����D

�ŏ��ɁC�֐�imnoise()��p���Ĕ����Z�W���摜�Ƀm�C�Y��Y�t����D

ORG = imnoise(ORG,'salt & pepper',0.02); % �m�C�Y�Y�t  

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_1.jpg)  
�}2 �m�C�Y��Y�t�����摜

��������́C�t�B���^��p���ēY�t�����m�C�Y����������D

�܂��C�������t�B���^��p���ăm�C�Y�������s���D

IMG = filter2(fspecial('average',3),ORG); % �������t�B���^�ŎG������

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_2.jpg)  
�}3 �������t�B���^��p���ăm�C�Y�������s�����摜

���ɁC���f�B�A���t�B���^��p���ăm�C�Y�������s���D

IMG = medfilt2(ORG,[3 3]); % ���f�B�A���t�B���^�ŎG������

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_3.jpg)  
�}3 ���f�B�A���t�B���^��p���ăm�C�Y�������s�����摜

�Ō�ɁC�쐬�����t�B���^��p���ăm�C�Y�������s���D�����ł́C�ȉ��̍s��f��p����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_matrix.gif)  

f=[0,-1,0;-1,5,-1;0,-1,0]; % �t�B���^�̐݌v  
IMG = filter2(f,IMG,'same'); % �t�B���^�̓K�p  

���̌��ʂ�}4�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai9_4.jpg)  
�}4 ���f�B�A���t�B���^��p���ăm�C�Y�������s�����摜