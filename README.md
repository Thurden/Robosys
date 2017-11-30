# Robosysi
Device driver fro Rasberrypi 3

# 概要
このリポジトリはLinuxドライバのリソースが含んでいる  
そのデバイスドライバを使ってGPIOの出力をコントロールする

# 準備
* リナックスカーネルリソース  
* カーネルリソースを /usr/src/linux というディレクトリにダウンロードする  
  　* カーネルビルドスクリプト:[https://github.com/ryuichiueda/raspberry_pi_kernel_build_scripts]  
* ラズベリーパイ 2 また　ラズベリーパイ 3  
   * 私はラズベリーパイ 3でこの実験を行った  
* LED  
* resistor  
  * 330[Ω]  
  * 10k[Ω]  

# 使用方法
* myled.cを指定のディレクトリにgit clone2で複製する    
* GPIOに出力を出す方法  
    * make //コンパイル  
    * sudo insmod myled.ko //カーネルモジュールの脱着  
    * udo chmod 666 /dev/myled0 //デバイスファイルの操作権限を与える  
    * echo 1 > /dev/myled0   //指定のピンに電圧を出力する、LEDが点灯  
    * echo 0 > /dev/myled0  //LEDが消灯  


# LED点灯実験動画  
[LED点灯](https://www.youtube.com/watch?v=u6zmz3Zq5E0)

# ライセンス  
This reposity is licensed under GPLv3 license
