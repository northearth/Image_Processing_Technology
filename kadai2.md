# �ۑ�2���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��  

�ɂ���āC���摜��ǂݍ��݁C�����Z�W�摜�ɕϊ����C�\���������ʁi�ȉ��C�����Z�W���摜�j��}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_0.jpg)  
�}1 �����Z�W���摜

�����Z�W���摜��2�K���̉摜�ɕϊ�����ɂ́C�摜�Ɋ܂܂��K�����P�x�l�Ɋւ���2��ނɕ��ނ���΂悢�D

���Ȃ킿�C�����Z�W���摜�͋P�x�l�Ɋւ���256�̊K�������摜�ł��邩��C�P�x�l��128�𒴂�����̂��C����ȊO���ɕ��ނ���΂悢�D

IMG = ORG>128; %�K�����P�x�l�Ɋւ���2�ɕ���

2�K���������s�����̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_1.jpg)  
�}2 2�K���摜

���l��,�����Z�W���摜��4�K���̉摜�ɕϊ�����ɂ́C�摜�Ɋ܂܂��K�����P�x�l�Ɋւ���4��ނɕ��ނ���΂悢�D���������āC

IMG0 = ORG>64; %�P�x�l����64�𒴂�128�ȉ��̂���  
IMG1 = ORG>128; %�P�x�l��128�𒴂�192�ȉ��̂���  
IMG2 = ORG>192; %�P�x�l��192�𒴂������ 

�����ŁC���ނ����摜����̉摜�Ƃ��Č�������D����킿�C

IMG = IMG0 + IMG1 + IMG2;  

�Ƃ���D4�K���������s�����̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_2.jpg)  
�}3 4�K���摜

�܂��C8�K���̉摜�͈ȉ��̏����ɂ���ĕϊ��ł���D

IMG00 = ORG>32; %�P�x�l��32�𒴂�64�ȉ��̂���  
IMG01 = ORG>64; %�P�x�l��64�𒴂�96�ȉ��̂���  
IMG02 = ORG>96; %�P�x�l��96�𒴂�128�ȉ��̂���  
IMG03 = ORG>128; %�P�x�l��128�𒴂�160�ȉ��̂���  
IMG04 = ORG>160; %�P�x�l��160�𒴂�192�ȉ��̂���  
IMG05 = ORG>192; %�P�x�l��192�𒴂�224�ȉ��̂���  
IMG06 = ORG>224; %�P�x�l��224�𒴂������  
IMG = IMG00 + IMG01 + IMG02 + IMG03 + IMG04 + IMG05 + IMG06; %�摜�̌���  

8�K���������s�����̌��ʂ�}4�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai2_3.jpg)  
�}4 8�K���摜

���̂悤�ɊK���������Ă����ƁC��ʑ̂̉��ʂ�`��Ȃǂ��͂�����Ƌ�ʂł���悤�ɂȂ邱�Ƃ��킩��D
