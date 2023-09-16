` ngrok config add-authtoken <token-ngrok> `\
nano /root/.config/ngrok/ngrok.yml \
` version: "2" `\
` authtoken: <ngrok-token> `\
` tunnels: `\
`  web blog: `\
`    addr: 8080 `\
`    proto: http `\
`  ssh-access: `\
`    addr: 22 `\
`    proto: tcp `\
   
