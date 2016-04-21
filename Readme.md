﻿
## CreateLwi

L-SMASH Worksのlwiファイルを作成します。


------------------------------------------------------------------
### 使い方

Run_CreateLwi.batのショートカットを作成し、TSファイルをドロップ


### 使い方　　コマンドライン

ファイル  
CreateLwi.exe  "C:\video.ts"

パイプ  
CreateLwi.exe  -pipe "C:\video.ts"



------------------------------------------------------------------
### 引数

    -file  "C:\video.ts"  
入力ファイル名


    -pipe  "C:\video.ts"  
パイプからデータを受けとる  
lwiファイル内の`<InputFilePath>`にC:\video.tsを書き込みます。  


    -lwi  "C:\video.ts"  
lwiファイルの出力名を指定  
拡張子.lwiがなければ付加されます。  
-lwiがなければ入力ファイル名からlwiファイル名を作成します。  
文字コード　shift-jis, binary


    -footer  
lwiのフッターを出力  
-pipeが指定されているときのみ定期的にfooter部分を出力します。  
文字コード　shift-jis, binary


    -ref_filename  
lwiファイル内の`<InputFilePath>`にフルパスでなくファイル名を書き込みます。


    -limit 10.0  
ファイル読込み速度を 10.0MiB/secに制限



------------------------------------------------------------------
### 注意点

* 引数-fileと-pipeで作成したインデックスは同一のファイルにならないときがあります。  
（いくつかのPTS,DTS値が異なる。）  
また、PTS,DTSの大部分が異なる場合を確認しています。
値は異なりますが変化の仕方はほとんどが同じで問題なく使用できます。
それに伴いファイルサイズも大きく変わります。



------------------------------------------------------------------
### 謝辞
based on L-SMASH Works AviSynth r785
L-SMASH Worksからインデックス作成部分のみを実行ファイルにしました。  
Yusuke Nakamura/VFR-maniacさん及び開発に関わった方々にお礼申し上げます。


LSW 各プラグイン作成までは、  
drocon11さんのlw-build及び、MaverickTseさんのlsw-build2  
を利用させていただきました。お礼申し上げます。


    Copyright (C) 2012-2015 L-SMASH Works project

    Avisynth v2.5.  Copyright 2002 Ben Rudiak-Gould et al.
    http://www.avisynth.org

    Copyright (c) 2000-2015 the FFmpeg developers  
    https://www.ffmpeg.org/  
    https://github.com/FFmpeg/FFmpeg  

    
------------------------------------------------------------------
### ライセンス

    GPL v3
    Copyright (C) 2014  CHATRA
    http://www.gnu.org/licenses/

