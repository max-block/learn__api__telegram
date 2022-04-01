https://core.telegram.org/bots/api


echo BOT_TOKEN=*********:************************
echo CHAT_ID=*********

# get bot's info
xh https://api.telegram.org/bot${BOT_TOKEN}/getMe

# send message
curl -X POST \
     -H 'Content-Type: application/json' \
     -d '{"chat_id": "${CHAT_ID}", "text": "This is a test from curl"}' \
     https://api.telegram.org/bot${BOT_TOKEN}/sendMessage