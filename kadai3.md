# �ۑ�3���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_0.jpg)  
�}1 �����Z�W���摜

�����ł́C�P�x�l��4�p�^�[���ݒ肵�C臒l�������s���D

�͂��߂ɁC�P�x�l64��臒l�Ƃ���臒l�������s���D

IMG = ORG > 64; % �P�x�l��64�𒴂����f��1�C���̑���0�ɕϊ�

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_1.jpg)  
�}2 臒l64�ł�臒l�����摜

���ɁC�P�x�l96��臒l�Ƃ���臒l�������s���D

IMG = ORG > 96; % �P�x�l��96�𒴂����f��1�C���̑���0�ɕϊ�

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_2.jpg)  
�}3 臒l96�ł�臒l�����摜

�����āC�P�x�l128��臒l�Ƃ���臒l�������s���D

IMG = ORG > 128; % �P�x�l��128�𒴂����f��1�C���̑���0�ɕϊ�

���̌��ʂ�}4�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_3.jpg)  
�}4 臒l128�ł�臒l�����摜

�Ō�ɁC�P�x�l192��臒l�Ƃ���臒l�������s���D

IMG = ORG > 192; % �P�x�l��192�𒴂����f��1�C���̑���0�ɕϊ�

���̌��ʂ�}5�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai3_4.jpg)  
�}5 臒l192�ł�臒l�����摜

�����Z�W�摜�ł́C�P�x�l0�𔒁C�P�x�l256�����Ƃ��C���̊Ԃ�256�����ɕ������Z�W��\�����Ă���D

��L��������ǂݎ���悤�ɁC臒l��ω������邱�ƂŁC�摜���̔��ƍ��̊������ω����Ă��邱�Ƃ��킩��D
