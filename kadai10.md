# �ۑ�10���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_0.jpg)  
�}1 �����Z�W���摜

�����ł́C�G�b�W���o��̌�����D

�ŏ��ɁC�v���E�B�b�g�@��p���ăG�b�W���o���s���D

IMG = edge(ORG,'prewitt'); % �G�b�W���o�i�v���E�B�b�g�@�j

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_1.jpg)  
�}2 �v���E�B�b�g�@��p�����G�b�W���o�����摜

���ɁC�\�x���@��p���ăG�b�W���o���s���D

IMG = edge(ORG,'sobel'); % �G�b�W���o�i�\�x���@�j

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_2.jpg)  
�}3 �\�x���@��p�����G�b�W���o�����摜

�Ō�ɁC�L���j�[�@��p���ăG�b�W���o���s���D

IMG = edge(ORG,'canny'); % �G�b�W���o�i�L���j�[�@�j

���̌��ʂ�}4�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai10_3.jpg)  
�}4 �L���j�[�@��p�����G�b�W���o�����摜

���̂悤�ɁC�l�X�ȕ��@��p���ĉ摜�̃G�b�W���o���s�����Ƃ��ł��邱�Ƃ��킩��D