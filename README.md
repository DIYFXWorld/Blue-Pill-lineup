# Blue Pill lineup

## STM32F103C8

|Core     |FPU |System Clock|Program Flash|SRAM|ADC      |DAC |
|----     |----|----        |----         |----|----     |----|
|Cortex-M3|None|72MHz       |64k          |20k |ADC(1M)x2|None|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_1.jpg width=300 align=left>

Cortex-M3�R�A�ł��B 
Cortex-M3��FPU�������̂Ńn�[�h�E�F�A�Ŏ����v�Z�ł��܂���B
��͂�MCU�ł���2�n����ADC�������Ă���͍̂����_�ŁA
1�n�����I�[�f�B�I���͂ɁA����1�n�����ϒ�R�̓ǂݎ��Ɏg�������o���܂��B
�V���O���G�t�F�N�g�̎���ɓK���Ă���Ǝv���܂��B
DAC�͂���܂��񂪃G���L�M�^�[�p�ł����PWM���g�����^��DAC�ł��\���ł��B
�I�[�o�[�N���b�N��128MHz�܂ŃC�P�܂������M���傫���̂ł��Ȃ������ǂ��ł��B
I2S�������̂ŊO���R�[�f�b�N�̗��p�͓���ł��B
<br clear=all>

----

## STM32F303CC

|Core     |FPU |System Clock|Program Flash|SRAM  |ADC      |DAC  |
|----     |----|----        |----         |----  |----     |---- |
|Cortex-M4|Yes |72MHz       |256k         |40k+8k|ADC(5M)x4|DACx2|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_2.jpg width=300 align=left>
Cortex-M4��FPU�����Ńv���O������float(�P���x���������_)�����ʂɎg����̂�
�Œ菬���_���ƃI�T���o�ł��܂��B 
F103C8�Ƃ̓s���R���p�`�ł��B
ADC��5�n�������荷�����͂��ł��܂��B
���C��I2S��I�y�A���v��������Ă�����Ɣ��ɑ��@�\��MCU�ł����A
���ꂾ�����@�\���Ƌt�Ɏg�����Ȃ�����ςł��B
�]��~���炸��F103C8�̃��������ʔł��炢�Ɍ���̂��ǂ��Ǝv���܂��B
ADC��5MHz�܂ŃT���v�����O�ł���̂�40kHz��120�{�I�[�o�[�T���v�����O(4.8MHz)�ɂ�����A
���ꂾ���ŕ��ח���25%�𒴂��Ă��܂��܂����B
SN��F103���������ǂ��Ȃ�܂������A
���̕��ח��ł͓����Ȃ��v���O���������������ł��B
�I�[�o�[�N���b�N��128MHz�܂ŃC�P�܂������A
��͂蔭�M���傫���̂ł��Ȃ������ǂ��ł��B
<br clear=all>

----

