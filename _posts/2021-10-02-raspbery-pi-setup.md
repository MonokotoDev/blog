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
`node-red-start`してNode-REDが起動することを確認、その後に`node-red-stop`しておく。


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

# Deploy Node-RED application (A)
```
$ cd /home/pi/.node-red
$ mkdir projects
```
ProductionStateCardリポジトリを指定してプロジェクトをロードする。

```
$ cd /home/pi/.node-red
$ cp projects/ProductionStateCard/deploy/package.json .
$ npm install
```

# Deploy Node-RED application (B)
```
$ mkdir /home/pi/.node-red/projects
$ cd /home/pi/.node-red/projects
$ git clone https://github.com/MonokotoDev/ProductionStateCard.git
$ cd ProductionStateCard/deploy
$ cp package.json settings.js .config.projects.json .config.users.json /home/pi/.node-red
$ cd /home/pi/.node-red
$ npm install
```

# Mount NFS
```
sudo mount -t nfs 52.71.121.91:/home/aigaiot/node-red-db /mnt
```

# Start Node-RED
```
$ node-red-start
```
