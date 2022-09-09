# Botneartelegram
This script was created to Notify Near Validators about state changes in their nodes
Created by Aleksey Morozov



Installation:
Clone repository & install dependencies

git clone https://github.com/antoninab4/Botneartelegram

cd near-node-tg-bot

npm i
Make your config.env file by example .env

cp .env config.env
Set your settings to config.env

nano config.env

# set your values
TG_API_KEY=""
TG_CHAT_ID=""
NODE_RPC="127.0.0.1:3030"
POOL_ID="xxx.factory.shardnet.near"
TG_API_KEY - you can get from @BotFather
TG_CHAT_ID - you can by using @GetIDs Bot
Run
node index.js
To automate running script find path to Node.js
which node

# use this path to in crontask
> /usr/bin/node
Add chron task every minute

crontab -e
Add this row with setting path to Node.js and script

# set your path
*/1 * * * * cd /home/<USERNAME>/near-node-tg-bot/ && /usr/bin/node index.js > /dev/null 2>&1
Reload cron service to start execute script

sudo service cron reload
