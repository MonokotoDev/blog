# Software update
```
$ sudo apt update
$ sudo apt full-upgrade -y
$ sudo apt autoremove -y
$ sudo apt clean
$ sudo reboot
```

# Japanese input environment
```
$ sudo apt-get install ibus-mozc
```

# Install Node-RED
https://nodered.org/docs/getting-started/raspberrypi

```
$ node -v
v10.24.0
$ bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered) --node14
$ node -v
v14.18.0
$ node-red --help
Node-RED v2.0.6
```
# Setting Node-RED
プロジェクト機能をONにする。
`node-red-start`
プロジェクトを登録
gitの情報とか入れる。
プロジェクト設定→フローに設定 `system-ui-flow.json`
依存関係の設定→プロジェクトへ追加 `node-red-node-smooth`

testは閉じる必要あり。
これもnodeいれる。
BLE Beacon Scanner
Ambient
