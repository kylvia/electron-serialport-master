# 基于electron的桌面串口工具
准备工作
npm install -g cnpm --registry=https://registry.npm.taobao.org


npm install --global --production windows-build-tools

Set path=%path%;C:\Users\SP0014\.windows-build-tools\python27

npm config set python /path/to/executable/python2.7

cnpm i electron -g

cnpm install -g node-gyp

cnpm install 

cd .\\node_modules\\serialport\\

node-gyp configure --msvs_version=2015

node-gyp rebuild --target=1.6.2 --arch=x64 --target_arch=x64 --dist-url=https://npm.taobao.org/mirrors/atom-shell  

node-gyp rebuild --target=1.6.2 --arch=x64 --target_arch=x64 --dist-url=https://atom.io/download/electron

打包

"scripts": {

	"package": "electron-packager ./app electron-serialport --win --out electron-serialport --arch=x64 --electron--version 2.0.2 --overwrite --ignore=node_modules"
  
  },
  
cnpm install --save-dev electron-packager

cnpm run-script packager
