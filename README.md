# Blue Pill-lineup

### F103C8

|Core     |FPU |System Clock|Program Flash|SRAM|ADC      |DAC |
|----     |----|----        |----         |----|----     |----|
|Cortex-M3|None|72MHz       |64k          |20k |ADC(1M)x2|None|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_1.jpg width=300>

Cortex-M3コアです。 
Cortex-M3はFPUが無いのでハードウェアで実数計算できません。
非力なMCUですが2系統のADCを持っているのは高得点で、
1系統をオーディオ入力に、もう1系統を可変抵抗の読み取りに使う事が出来ます。
シングルエフェクトの自作に適していると思います。
DACはありませんがエレキギター用であればPWMを使った疑似DACでも十分です。
オーバークロックは128MHzまでイケますが発熱が大きいのでしない方が良いです。
I2Sが無いので外部コーデックの利用は難しいです。

----
