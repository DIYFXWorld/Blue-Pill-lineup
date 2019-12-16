# Blue Pill lineup

## STM32F103C8

|Core     |FPU |System Clock|Program Flash|SRAM|ADC      |DAC |
|----     |----|----        |----         |----|----     |----|
|Cortex-M3|None|72MHz       |64k          |20k |ADC(1M)x2|None|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_1.jpg width=300 align=left>

Cortex-M3コアです。 
Cortex-M3はFPUが無いのでハードウェアで実数計算できません。
非力なMCUですが2系統のADCを持っているのは高得点で、
1系統をオーディオ入力に、もう1系統を可変抵抗の読み取りに使う事が出来ます。
シングルエフェクトの自作に適していると思います。
DACはありませんがエレキギター用であればPWMを使った疑似DACでも十分です。
オーバークロックは128MHzまでイケますが発熱が大きいのでしない方が良いです。
I2Sが無いので外部コーデックの利用は難しいです。
<br clear=all>

----

## STM32F303CC

|Core     |FPU |System Clock|Program Flash|SRAM  |ADC      |DAC  |
|----     |----|----        |----         |----  |----     |---- |
|Cortex-M4|Yes |72MHz       |256k         |40k+8k|ADC(5M)x4|DACx2|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_2.jpg width=300 align=left>
Cortex-M4はFPU内蔵でプログラムでfloat(単精度浮動小数点)が普通に使えるので
固定小数点数とオサラバできます。 
F103C8とはピンコンパチです。
ADCが5系統もあり差動入力もできます。
何気にI2Sやオペアンプを内蔵していたりと非常に多機能なMCUですが、
これだけ多機能だと逆に使いこなしが大変です。
余り欲張らずにF103C8のメモリ増量版くらいに見るのが良いと思います。
ADCは5MHzまでサンプリングできるので40kHzの120倍オーバーサンプリング(4.8MHz)にしたら、
それだけで負荷率が25%を超えてしまいました。
SNはF103よりも少し良くなりましたが、
この負荷率では動かないプログラムが増えそうです。
オーバークロックは128MHzまでイケましたが、
やはり発熱が大きいのでしない方が良いです。
<br clear=all>

----

