# Lineup - Blue Pill

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

## STM32F411CE

|Core     |FPU |System Clock|Program Flash|SRAM  |ADC        |DAC  |
|----     |----|----        |----         |----  |----       |---- |
|Cortex-M4|Yes |100MHz      |512k         |40k+8k|ADC(2.4M)x1|None |

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_3.jpg width=300 align=left>

SRAM��128k����΃f�B���C�^�C�����^�b�v�����܂��B 
�ŏ��̓I�[�o�[�N���b�N�o���Ȃ��Ĕ߂��������̂ł����A 
CubeMX�̃C�^�Y����RCC��Flash Latency�������0WS�ɕύX���āA
�R���������ŃI�[�o�[�N���b�N�o���Ȃ��ƕ�����܂����B 
�t���b�V���̃A�N�Z�X���x��100MHz���炢������Ȃ񂾂����ŁA 
Flash Latency��0 Wait�ł�100MHz�𒴂���N���b�N�ݒ�͓����܂���B 
Flash Latency��100MHz�܂łȂ�0WS�A100MHz�𒴂���Ȃ�2WS(3 CPU Cycle)�ȏ�ɐݒ肵�܂��B 
�I�[�o�[�N���b�N��128MHz�܂ł͊m�F���܂����B 
128MHz�I�[�o�[�N���b�N�ł̔��M�͏��Ȃ��ł��B 
����ADC��SN�͂��܂�ǂ��Ȃ�50�{�I�[�o�[�T���v�����O�ł��A 
�I�[�o�[�N���b�N����F103�Ɠ����������������炢�Ŕ߂����ł��B 
�f���ɊO���R�[�f�b�N��t����̂��ǂ��ł��B
SN��ADC���x�z�I�Ȃ̂ŁAADC�����R�[�f�b�N�ɂ��āADAC��PWM�^��DAC�ł��\���ł��B 
�V�X�e���N���b�N��128MHz�������PWM�^��DAC�̃L�����A��500kHz�ɂȂ�܂��B

----

## STM32F407VE/VG

|      |Core     |FPU |System Clock|Program Flash|SRAM    |ADC        |DAC  |
|----  |----     |----|----        |----         |----    |----       |---- |
|F407VE|Cortex-M4|Yes |168MHz      |512k         |128k+64k|ADC(2.4M)x3|DACx2|
|F407VG|Cortex-M4|Yes |168MHz      |1M           |128k+64k|ADC(2.4M)x3|DACx2|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_4.jpg width=300 align=left>

F407VE/VG�̓I�[�o�[�N���b�N��216MHz���炢�̓C�P�܂��B 
200MHz����Όy���G�t�F�N�g�ł����4���񂭂炢�͓������܂��B 
�����傫�߂̃P�[�X�ɓ���Ė{�i�I�ȃ}���`�G�t�F�N�^�[����ꂻ���ł��B 
SD�J�[�h�X���b�g��4�r�b�gSDIO�Őڑ�����Ă��܂��̂�SPI���4�{�����ł��B 
64k������CCMSRAM�̓|�C���^�ŃA�h���X�w�肷��Ε��ʂ̃������Ƃ��ēǂݏ����ł��܂��B 
����SRAM�̈�Ƃ͘A�����Ă��Ȃ��̂ŒP��64k�u���b�N�Ƃ��Ă����g���܂��񂪁A 
64k������΃f�B���C�A���o�[�u�p�ł����Ȃ��ł��傤�B

----

## STM32H750VB/H743VI

|      |Core     |FPU |System Clock|Program Flash|SRAM    |ADC               |DAC  |
|----  |----     |----|----        |----         |----    |----              |---- |
|H750VB|Cortex-M7|Yes |480MHz      |128k         |1M      |ADC(1.2M)x3(16bit)|DACx2|
|F743VI|Cortex-M7|Yes |480MHz      |1M           |128k+64k|ADC(2.4M)x3|DACx2|

����Cortex-M7�ł��B���AH750VB�̓��[�v���C�X�̃o�����[���C���V���[�Y��
�t���b�V������������128k��������܂���B
���E���E��E��B�Ȃ�Ƃ����A���o�����X�B�ق�Ƃ̎��p�v���Z�b�T�Ȃ�ł��傤�B

ADC���ڏo�x��16�r�b�g�ɂȂ�܂����B��ŏЉ���v���Z�b�T��ADC�͑S��12�r�b�g�ł��B
12�r�b�g�𑜓x�ł̓I�[�f�B�I�p�Ƃ��Ă��̂܂܎g���̂͌������̂ŁA�I�[�o�[�T���v�����O����Ƃ��A
�O���R�[�f�b�N��t����Ƃ����������̑Ώ����K�v�ł��B
�����l����ƃ����`�b�v�ŃC�P�Ă��܂�H750�͂����͈����͂Ȃ��̂�������܂���B

�������̃n�C�p���[�����Ɏg�����H�����ł��B�X�e���I�d�l�ɂ���Ȃ�ʂł����A
�M�^�[�G�t�F�N�^�[�œƗ�2�n���ܑ͖̂Ȃ��ł��傤�B
�ǂ�ǂ�@�\���l�ߍ���ł�����̂͗ǂ����ǂ��̕��v���O���}�[�͑�ςȂ�ł���B


