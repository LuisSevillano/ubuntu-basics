# ubuntu-basics
a few dependencies to start working on ubuntu
* google chrome
* nodejs
* [npm tool packages](https://www.npmjs.com/)
* [node http-server](https://www.npmjs.com/package/http-server)
* git
* [topojson](https://github.com/mbostock/topojson)
* [mapshaper command line tool](https://github.com/mbloch/mapshaper)
* [qgis](http://www.qgis.org/es/site/)
* [atom editor](https://atom.io/)
* [telegram desktop (spanish)](https://www.atareao.es/ubuntu/instalar-telegram-en-espanol-y-desde-repositorio-en-ubuntu/)

thinking on copy and paste the huge code below on your terminal and executes in _one_ command. If you want to install one by one just remove the ```&&``` symbols. Yes, Its a weird and crazy way to do this.
All dependencies works at the time of this initial commit for ```ubuntu 16.04```.

```bash
sudo wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - &&
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list' &&
sudo apt-get update &&
sudo apt-get install google-chrome-stable &&
sudo apt-get install nodejs &&
sudo apt-get install npm &&
sudo apt-get install git &&
sudo npm install http-server -g &&
npm install -save--dev topojson &&
npm install -save--dev mapshaper &&
sudo apt-get update &&
sudo add-apt-repository ppa:webupd8team/atom &&
sudo apt-get install atom &&
sudo add-apt-repository ppa:atareao/telegram &&
sudo apt-get update &&
sudo apt-get install telegram &&
sudo sh -c 'echo "deb http://qgis.org/debian xenial main" >> /etc/apt/sources.list'  &&
sudo sh -c 'echo "deb-src http://qgis.org/debian xenial main " >> /etc/apt/sources.list' &&
wget -O - http://qgis.org/downloads/qgis-2016.gpg.key | gpg --import &&
gpg --fingerprint 073D307A618E5811 &&
gpg --export --armor 073D307A618E5811 | sudo apt-key add - &&
sudo apt-get update && sudo apt-get install qgis python-qgis
```
