# �ۑ�8���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai8_0.jpg)  
�}1 �����Z�W���摜

�����ł́C��l�����s�����摜�̘A�������Ƀ��x��������D

�܂��C�P�x�l128��臒l�Ƃ��ĉ摜�̓�l�����s���D

IMG = ORG > 128; % 臒l128�œ�l��

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai8_1.jpg)  
�}2 ��l�����s���������Z�W���摜

�����ŁC�֐�bwlabeln()��p���ĘA�������Ƀ��x���t�����s���D

IMG = bwlabeln(IMG); 

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai8_2.jpg)  
�}3 ���x���t���������s�����摜

���̂悤�ɁC���x���t�����s�����Ƃɂ���āC��l�������摜�����ł͂킩��Ȃ��摜���̏�Ԃ����o�I�ɑ����邱�Ƃ��ł���D