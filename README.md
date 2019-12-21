# Lineup - Blue Pill

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

## STM32F411CE

|Core     |FPU |System Clock|Program Flash|SRAM  |ADC        |DAC  |
|----     |----|----        |----         |----  |----       |---- |
|Cortex-M4|Yes |100MHz      |512k         |40k+8k|ADC(2.4M)x1|None |

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_3.jpg width=300 align=left>

SRAMが128kあればディレイタイムもタップリ取れます。 
最初はオーバークロック出来なくて悲しかったのですが、 
CubeMXのイタズラでRCCのFlash Latencyを勝手に0WSに変更して、
コレが原因でオーバークロック出来ないと分かりました。 
フラッシュのアクセス速度は100MHzくらいが上限なんだそうで、 
Flash Latencyが0 Waitでは100MHzを超えるクロック設定は動きません。 
Flash Latencyは100MHzまでなら0WS、100MHzを超えるなら2WS(3 CPU Cycle)以上に設定します。 
オーバークロックは128MHzまでは確認しました。 
128MHzオーバークロックでの発熱は少ないです。 
内蔵ADCのSNはあまり良くなく50倍オーバーサンプリングでも、 
オーバークロックしたF103と同じか少し悪いくらいで悲しいです。 
素直に外部コーデックを付けるのが良いです。
SNはADCが支配的なので、ADCだけコーデックにして、DACはPWM疑似DACでも十分です。 
システムクロックが128MHzもあればPWM疑似DACのキャリアは500kHzになります。

----

## STM32F407VE/VG

|      |Core     |FPU |System Clock|Program Flash|SRAM    |ADC        |DAC  |
|----  |----     |----|----        |----         |----    |----       |---- |
|F407VE|Cortex-M4|Yes |168MHz      |512k         |128k+64k|ADC(2.4M)x3|DACx2|
|F407VG|Cortex-M4|Yes |168MHz      |1M           |128k+64k|ADC(2.4M)x3|DACx2|

<img src=https://github.com/DIYFXWorld/Blue-Pill-lineup/blob/master/image/photo_4.jpg width=300 align=left>

F407VE/VGはオーバークロックで216MHzくらいはイケます。 
200MHzあれば軽いエフェクトであれば4直列くらいは動かせます。 
少し大きめのケースに入れて本格的なマルチエフェクターも作れそうです。 
SDカードスロットは4ビットSDIOで接続されていますのでSPIより4倍速いです。 
64kもあるCCMSRAMはポインタでアドレス指定すれば普通のメモリとして読み書きできます。 
他のSRAM領域とは連続していないので単独64kブロックとしてしか使えませんが、 
64kもあればディレイ、リバーブ用でも問題ないでしょう。

----

## STM32H750VB/H743VI

|      |Core     |FPU |System Clock|Program Flash|SRAM    |ADC               |DAC  |
|----  |----     |----|----        |----         |----    |----              |---- |
|H750VB|Cortex-M7|Yes |480MHz      |128k         |1M      |ADC(1.2M)x3(16bit)|DACx2|
|F743VI|Cortex-M7|Yes |480MHz      |1M           |128k+64k|ADC(2.4M)x3|DACx2|

遂にCortex-M7です。が、H750VBはロープライスのバリューラインシリーズで
フラッシュがたったの128kしかありません。
い・じ・わ・る。なんというアンバランス。ほんとの試用プロセッサなんでしょう。

ADCも目出度く16ビットになりました。上で紹介したプロセッサのADCは全て12ビットです。
12ビット解像度ではオーディオ用としてそのまま使うのは厳しいので、オーバーサンプリングするとか、
外部コーデックを付けるとか何がしかの対処が必要です。
そう考えるとワンチップでイケてしまうH750はそうは悪くはないのかもしれません。

ただこのハイパワーを何に使うか？が問題です。ステレオ仕様にするなら別ですが、
ギターエフェクターで独立2系統は勿体ないでしょう。
どんどん機能を詰め込んでいけるのは良いけどその分プログラマーは大変なんですよ。


