# �ۑ�7���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai7_0.jpg)  
�}1 �����Z�W���摜

�����ł́C��f�̃_�C�i�~�b�N�����W��0����255�ɕύX����D

�܂��C�������s���O�̔Z�W�������摜�̃q�X�g�O������}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai7_1.jpg)  
�}2 �����Z�W���摜�̃q�X�g�O����

��������C�_�C�i�~�b�N�����W�̕ύX���s���D

�܂��C�P�x�l�𐮐��z�񂩂�{���x�z��ɕϊ����s���D

ORG = double(ORG);  

���ɁC�P�x�l�̍ő�l�E�ŏ��l���Z�o���C�_�C�i�~�b�N�����W��ύX����D

mn = min(ORG(:)); % �Z�x�l�̍ŏ��l���Z�o  
mx = max(ORG(:)); % �Z�x�l�̍ő�l���Z�o  
ORG = (ORG-mn)/(mx-mn)*255;  

���̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai7_2.jpg)  
�}3 �_�C�i�~�b�N�����W��ύX�����������摜

���̉摜�ɑ΂��āC�P�x�l��{���x�z�񂩂�8�r�b�g�����Ȃ������ւ̕ϊ����s���D����́C�֐�imhist()���K��̐ݒ��256�̃r�����g�p���Ă��邱�ƂɋN������D

ORG = uint8(ORG);  

���̏����̌�C�֐�imhist()��p���ĉ�f�̔Z�x�q�X�g�O�����𐶐����C�\������D

imhist(ORG); % �q�X�g�O�����̕\��

���̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai4_1.jpg)  
�}2 �_�C�i�~�b�N�����W��ύX�����������摜�̃q�X�g�O����

�Ȃ��C�@�O�q�̏������s�킸�Ƀq�X�g�O�����𐶐����悤�Ƃ��Ă��\�����邱�Ƃ͂ł��Ȃ��D

����̏ꍇ�́C�����Z�W���摜�����Ƃ���0����255�̋P�x�l�����摜�ł��������Ƃ���C�����̑O��ŕω��͌����Ȃ������D

�P�x�l���Z���͈͂ɏW�����Ă���摜��p���邱�ƂŁC�ω����݂���ƍl������D