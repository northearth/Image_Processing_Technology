# �ۑ�1���|�[�g

�摜�uYokohama_View.JPG�v�����摜�Ƃ���D���̉摜�͏c1210�摜�C��1613��f�ɂ�钷���`�̃f�B�W�^���J���[�摜�ł���D

ORG=imread('Yokohama_View.JPG'); % ���摜�̓���  
imagesc(ORG); axis image; % �摜�̕\��

�ɂ���āC���摜��ǂݍ��݁C�\���������ʂ�}1�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/Yokohama_View.JPG)  
�}1 ���摜

���摜��1/2�T���v�����O����ɂ́C�摜��1/2�{�ɏk��������C2�{�Ɋg�傷��΂悢�D�Ȃ��C�g�傷��ۂɂ́C�P����Ԃ��邽�߂Ɂubox�v�I�v�V������ݒ肷��D

IMG = imresize(ORG,0.5); % �摜�̏k��  
IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

1/2�T���v�����O�̌��ʂ�}2�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai1_1.jpg)  
�}2 1/2�T���v�����O

���l�Ɍ��摜��1/4�T���v�����O����ɂ́C�摜��1/2�{�ɏk��������C2�{�Ɋg�傷��΂悢�D���Ȃ킿�C

IMG = imresize(ORG,0.5); % �摜�̏k��  
IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

�Ƃ���D1/4�T���v�����O�̌��ʂ�}3�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai1_2.jpg)  
�}3 1/4�T���v�����O

1/8����1/32�T���v�����O�́C

IMG = imresize(ORG,0.5); % �摜�̏k��  
IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

���J��Ԃ��D�T���v�����O�̌��ʂ�}4�`6�Ɏ����D

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai1_3.jpg)  
�}4 1/8�T���v�����O

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai1_4.jpg)  
�}5 1/16�T���v�����O

![���摜](https://github.com/northearth/Image_Processing_Technology/blob/master/image/kadai1_5.jpg)  
�}6 1/32�T���v�����O

���̂悤�ɃT���v�����O�����傫���Ȃ�ƁC���U�C�N��̃T���v�����O�c�݂���������D
