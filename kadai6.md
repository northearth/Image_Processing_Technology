# �ۑ�6���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai6_0.jpg)  
�}1 �����Z�W���摜

����́C2��ނ̕��@�ɂ���ē�l�����s���D

�܂��C臒l��p���ē�l�����s���D�����ł́C臒l��128�Ƃ���D

IMG = ORG>128; % 128�ɂ���l��  

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai6_1.jpg)  
�}2 臒l128�ł̓�l�������摜

���ɁC�f�B�U�@��p���������ɂ��C��l�����s���D

IMG = dither(ORG); % �f�B�U�@�ɂ���l��  

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai6_2.jpg)  
�}3 �f�B�U�@��p������l�������摜

���̂悤�ɁC�摜�̓�l���͏����̕��@�ɂ���Č��ʂ��قȂ邱�Ƃ��킩��D