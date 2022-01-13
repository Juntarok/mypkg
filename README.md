# mypkges

2年　未来ロボティクス学科　ロボットシステム学の課題2

# 目次
・目的

・使用機器

・実行手順

・インストール

・実行

・引用


# 目的

未来ロボティクス学科　セメスター４　ロボットシステム学の授業課題としてrasberry piを用いてROSを学ぶ


# 使用機器

・rasberry pi4

・rasberry pi4周辺機器

・パソコン

・LANケーブル


# 実行手順

1 linuxのウィンドウを四つ開く

2 sshしパソコンでログインする

3 cloneしインストールする

4 コマンドを打ち込み実行する


# インストール

    $ git clone https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server.git
    $ source step0.bash
    $ source step1.bash
  
次にcloneし「count2.py」と「twice.py」をインストールする

    $ git clone https://github.com/Juntarok/mypkges.git
    
# 実行

 まず一つ目のウィンドウで
 
    $ roscore
    
二つ目のウィンドウ

    $ cd mypkges
    $ cd scripts
    $ chmod +x count2.py
    $ rosrun mypkg count2.py
    
三つ目のウィンドウ

    $ cd mypkges
    $ cd scripts
    $ chmod +x twice.py
    $ rosrun mypkg twice.py
    
四つ目のウィンドウ

    $ rostopic echo /twice
    

「count2.py」と「twice.py」を実行すると「count2.py」で数字が表示されるものに「twice.py」で 2 ずつ足されていくプログラムになっている。


# 引用
Ryuichi Ueda https://youtu.be/PL85Pw_zQH0
