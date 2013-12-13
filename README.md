Run remote terminal commands using [Websocketd](https://github.com/joewalnes/websocketd)

##Get Websocketd (mac)
    wget http://download.websocketd.com/releases/websocketd/0.2.7/darwin_amd64/websocketd

## Start the server 
    ./websocketd --port=8080 --devconsole ./commands.sh

## Visit localhost 
    localhost:8080


## Run Commands 
press `enter` to connect and start running commands

ls

    onmessage» ls 
    onmessage README.md commands.sh websocketd 

pwd

    onmessage» pwd 
		onmessage /Users/ioannis/Development/websockets

whoami

		    onmessage» whoami 
				onmessage ioannis

with params

				onmessage» git init
				onmessage Initialized empty Git repository in /Users/ioannis/Development/websockets/.git/ 

with pipes

				onmessage» ls | grep READ 
				onmessage README.md 


assigning variables

								onmessage» var="my var" 
								onmessage» echo $var 
								onmessage my var
