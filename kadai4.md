# �ۑ�4���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai4_0.jpg)  
�}1 �����Z�W���摜

�����ŁC�֐�imhist()��p���ĔZ�W�������摜�̃q�X�g�O������\������D

imhist(ORG); % �q�X�g�O�����̕\��

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai4_1.jpg)  
�}1 �����Z�W���摜

�q�X�g�O��������ǂݎ���悤�ɁC����p���������Z�W���摜�ł́C

�P�x�l�������悻90����130�܂ł̂��̂������܂܂�Ă��邱�Ƃ��킩��D