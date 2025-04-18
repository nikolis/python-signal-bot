# python-signal-bot

## System 
![Alt text](diagrams/system.jpg?raw=true "Select Diagram")


## Setting up 
1) Register a new signal Account if not already there 
2) Connect the Signal Account that you are planning to use for the signal bot with the desktop-application 
  Verification Step 
3) Configure the Signal-Account for the Dockerized Signal Messenger REST API [link](https://github.com/bbernhard/signal-cli-rest-api) 
4) Run on rpc-mode 
```
   docker stop signal-api 
   docker remove signal-api
```

```sudo docker run -d --name signal-api --restart=always -p 8080:8080 \
      -v $HOME/.local/share/signal-api:/home/.local/share/signal-cli \
      -e 'MODE=json-rpc' bbernhard/signal-cli-rest-api) ```
