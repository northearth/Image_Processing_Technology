# �ۑ�2���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�O���[�X�P�[���ɕϊ����C�\���������ʁi�ȉ��C�O���[�X�P�[�����摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_0.jpg)  
�}1 �O���[�X�P�[�����摜

�O���[�X�P�[�����摜��2�K���̉摜�ɕϊ�����ɂ́C�摜�Ɋ܂܂��K����2��ނɕ�������K�v������D

�O���[�X�P�[�����摜�́C256�K���̉摜�ł��邩��C�K����0�ȏ�127�ȉ��̂��̂�128�ȏ�256�ȉ��ł�����̂ɕ�������΂悢�D

IMG = ORG>128; %�K����2�ɕ���

2�K���������s�����̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_1.jpg)  
�}2 2�K���摜

���l�ɃO���[�X�P�[�����摜��4�K���̉摜�ɕϊ�����ɂ́C�摜�Ɋ܂܂��K����4��ނɕ�������΂悢�D���������āC

IMG0 = ORG>64; %�K����65�ȏ�128�ȉ��̂���
IMG1 = ORG>128; %�K����129�ȏ�192�ȉ��̂���
IMG2 = ORG>192; %�K����193�ȏ�256�ȉ��̂���

�����ŁC���������K������̉摜�Ƃ��Č�������D����킿�C

IMG = IMG0 + IMG1 + IMG2;

�Ƃ���D4�K���������s�����̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_2.jpg)  
�}3 4�K���摜

���l�ɁC8�K���̉摜�͈ȉ��̏����ɂ���ĕϊ��ł���D

IMG00 = ORG>32; %�K����33�ȏ�64�ȉ��̂���

IMG01 = ORG>64; %�K����65�ȏ�96�ȉ��̂��́@
IMG02 = ORG>96; %�K����97�ȏ�128�ȉ��̂��́@
IMG03 = ORG>128; %�K����129�ȏ�160�ȉ��̂��́@
IMG04 = ORG>160; %�K����161�ȏ�192�ȉ��̂��́@
IMG05 = ORG>192; %�K����193�ȏ�224�ȉ��̂��́@
IMG06 = ORG>224; %�K����225�ȏ�256�ȉ��̂��́@
IMG = IMG00 + IMG01 + IMG02 + IMG03 + IMG04 + IMG05 + IMG06; %�@�摜�̌���

8�K���������s�����̌��ʂ�}4�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_3.jpg)  
�}4 8�K���摜

���̂悤�ɊK���������Ă����ƁC��ʑ̂̉��ʂ�`��Ȃǂ��͂�����Ƌ�ʂł���悤�ɂȂ邱�Ƃ��킩��D
