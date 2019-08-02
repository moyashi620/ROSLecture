# ROSを用いた4輪移動ロボットのナビゲーション

　予め，環境地図をLRFを用いて生成し，生成された環境地図をもとに目標位置を指定し，ロボットを移動させる．
<br>したがって，ここでは環境地図の生成については述べないものとする．

## gazeboの起動方法

1. ターミナル上で以下のように入力する．
```bash 
$ roslaunch wheel_robot wheel_robot.launch
```
2. 以下の画像のようにgazeboが起動する．また，4輪移動ロボットと走行環境であるwillowgarageが表示される．
<img src ="https://user-images.githubusercontent.com/53034346/62276100-451e3f80-b47e-11e9-9815-54c2d72acd7c.png">

## 自己位置推定用ノード(amcl)の起動方法

1. ターミナル上で以下のように入力する．
```bash 
$ roslaunch wheel_robot amcl.launch
```

2. ターミナル上でamclが起動し，画像のように表示されていれば起動成功．
<img src = "https://user-images.githubusercontent.com/53034346/62282201-1c9c4280-b48a-11e9-9b96-2d2740d667b7.png">

## rvizの起動方法と表示設定

1. ターミナル上で以下のように入力する．
```bash 
$ rosrun rviz rviz
```

2. 画像のようにrvizが起動する．
<img src = "https://user-images.githubusercontent.com/53034346/62364920-bd0f6700-b55d-11e9-8279-c0ccfe0cbb2f.png">

3. ロボットを表示させるために，起動直後の左下の"Add"をクリックする．<br>
By display typeタブでは"RobotModel"を，By topicタブでは"map/Map"と，"move_base/NavfnROS/plan/Path"を追加する．<br>
<img src = "https://user-images.githubusercontent.com/53034346/62365424-07451800-b55f-11e9-9106-a2115066840b.png">
<img src = "https://user-images.githubusercontent.com/53034346/62365456-1c21ab80-b55f-11e9-8ce6-a08d0d425081.png">

4. 追加すると，以下の画像のような状態になる．
<img src = "">