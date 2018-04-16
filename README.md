## steamhourboost v2

This new version natively supports two-factor authentication using the shared secret of your app.

To add new users to the `database.json` run `coffee user.coffee` and follow the instructions.

If you want to change the games that are being boosted, edit the `database.json` directly!

### How to install

```bash
wget --no-check-certificate "https://nodejs.org/dist/latest/node-$(curl -L 'nodejs.org/dist/index.tab' | sed -n '2p' | awk '{ print $1 }')-linux-x64.tar.gz" -O /tmp/nodejs.tar.gz
sudo tar --strip-components 1 -xzvf /tmp/nodejs.tar.gz -C /usr/local
sudo npm -g install npm@latest
sudo npm -g install coffee-script pm2
sudo pm2 install coffeescript
```

```bash
# If git is missing on your server google on how to install it.
# On Debian/Ubuntu the command is 'sudo apt-get install git'
git clone https://github.com/frk1/steamhourboostv2.git
```

`cd` into the folder and install the dependencies

```bash
cd steamhourboostv2
npm install .
```

### How to use


```bash
pm2 start boost.coffee
```

```bash
pm2 restart all
```

```bash
pm2 ls
```

