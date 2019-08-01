# ROSを用いた4輪移動ロボットのナビゲーション

　予め，環境地図をLRFを用いて生成し，生成された環境地図をもとに目標位置を指定し，ロボットを移動させる．
<br>したがって，ここでは環境地図の生成については述べないものとする．

## gazeboの起動方法

1. ターミナル上で以下のように入力する．
```bash 
$ roslaunch wheel_robot wheel_robot.launch
```
2. 以下の画像のようにgazeboが起動する．また，4輪移動ロボットと走行環境であるwillowgarageが表示される．
<br></br>
<img src ="https://user-images.githubusercontent.com/53034346/62276100-451e3f80-b47e-11e9-9815-54c2d72acd7c.png">

## 自己位置推定用ノード(amcl)の起動方法

1. ターミナル上で以下のように入力する．
```bash 
$ roslaunch wheel_robot amcl.launch
```

2. ターミナル上でamclが起動し，画像のように表示されていれば起動成功．
<br></br>
<img src = "https://user-images.githubusercontent.com/53034346/62282201-1c9c4280-b48a-11e9-9b96-2d2740d667b7.png">

## rvizの起動方法

1. ターミナル上で以下のように入力する．
```bash 
$ rosrun rviz rviz
```