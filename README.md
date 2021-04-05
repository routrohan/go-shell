# :desktop_computer: Go-shell - Your IRC playground

## :page_facing_up: Description

Go-shell is an experimental IRC client that runs entirely on the terminal. 
It is built using [Golang](https://golang.org/). The implementation is based on 
[TCP](https://searchnetworking.techtarget.com/definition/TCP#:~:text=TCP%20(Transmission%20Control%20Protocol)%20is,of%20data%20to%20each%20other.) standards. 
The app follows the standard procedures of any IRC server
(setting up nicknames, joining channels/rooms, broadcast etc). <br /> Hope you like it :)

## :hammer_and_wrench: Local Setup

### Requirements
1. To run the following application in your local machine, you need to have the following.<br />
 - A stable version of Golang (I used go1.16.3).
 - If you don't have Golang installed, find one that suits your OS [here](https://golang.org/dl/).
 - Check if Go is installed by running `go version`.
2. Telnet (to connect to the server)

### Build and Run
#### 1. To start the server
- Switch to the folder App in the project root `cd Go-shell/App`.
- Build the project `go build .`.
- Run the compiled file `/.main`.
- The server is up and running!<br /><br />
![server](https://github.com/routrohan/go-shell/blob/master/Screenshots/server_running.png)<br /><br />
#### 2. To interact within the app
- Open two different terminal sessions 
- Connect to `localhost:8888` using telnet: `telnet localhost 8888` and you are good to go!<br /><br />
![client](https://github.com/routrohan/go-shell/blob/master/Screenshots/client_connected.png)<br /><br />
The app has the following commands as of now:
1. `/nick` : Set your nickname
2. `/join` : Join a particular channel/room
3. `/rooms`: View all active rooms
4. `/msg`  : Send a message to all the users in the room 
5. `/quit` : Quit the app<br /><br />
An example of an interaction is given below:<br/><br/>
![clientint](https://github.com/routrohan/go-shell/blob/master/Screenshots/client_interact.png)

<b>Note<b/>: There are no rooms that are automatically created. The rooms are created only when the `/join` command is used (if the room has been created by another user then you will enter that room, else a fresh room will be created)
<br />
