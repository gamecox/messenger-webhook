## Facebook for Developers


### init
mkdir messenger-webhook
cd messenger-webhook
index.js
npm init
npm install express body-parser --save



### startup
cd ./messenger-webhook
npm install - install all dependencies in the package.json dependencies JSON object
npm start - reference to the 'package.json' scripts JSON object start command
https://localhost:1337 -- loopback server

## test
verification 
'sh
	curl -X GET "localhost:1337/webhook?hub.verify_token=<YOUR_VERIFY_TOKEN>&hub.challenge=CHALLENGE_ACCEPTED&hub.mode=subscribe"
'
test
'sh
	curl -h "Content-Type: application/json" -X POST "localhost:1337/webhook" -d '{"object": "page", "entry": [{"messaging: [{"message": "TEST_MESSSAGE"}]}]}'
'

## to-dos
 [] generate random string on both server and client

