# joe-server install

git clone https://github.com/miwnKEA/joe-server.git

cd joe-server

npm install

node app.js

## Node.js install

[Link til dokumentation](https://github.com/nodesource/distributions?tab=readme-ov-file#using-ubuntu-nodejs-18)

sudo apt-get install -y curl

curl -fsSL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh

sudo -E bash nodesource_setup.sh

sudo apt-get install -y nodejs

node -v

## pm2 install

sudo npm install pm2@latest -g

pm2 start app.js

pm2 startup systemd

sudo env PATH=$PATH:/usr/bin /usr/lib/node_modules/pm2/bin/pm2 startup systemd -u root --hp /home/root

pm2 save

sudo systemctl start pm2-root

systemctl status pm2-root

## pm2 kommandoer

pm2 list

pm2 start node_file.js

pm2 stop app_name_or_id

pm2 restart app_name_or_id

pm2 delete app_name_or_id

pm2 info app_name

pm2 save




