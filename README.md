# Alien
Alien is a fully end to end encrypted Chat, supporting multiple clients, using gpg's AES 256 cipher for encryption, and socat for data exchange, written entirely in bash

![alt text](https://i.imgur.com/oy43AYx.png)
![alt text](https://i.imgur.com/gzqCsn5.png)

Dependencies:
-
bash

socat

gnupg

Ussage:
-
```
git clone https://github.com/Tina-lel/Alien
```
## server:

```
cd Alien/server/
```
```
chmod +x *
```

open up "config" in a text editor and choose a port number to replace "1234" and "1235", and optionally forward these ports in your gateways configuration page, to communicate outside of your internal network

```
./server
```

see "Commands" for a list of valid commands

#### entering a password and running the server:

```
pass
```
the password file was generated in (script location)/gpg you should be careful with it
```
start
```
if everything went fine, and the server didn't return any errors, you can test the connection with a client

## client:

```
cd Alien/client/
```
```
chmod +x *
```

open up "config" in a text editor and change the "NAME" var. next edit the "HOST", "PORT" and "IPORT" variable, to point to a machine running the "server" script, on the same ports

```
./client
```
enter the server's password

if the server was running, and everything went fine, you should now see a blank screen, with a blinking cursor.

in order to chat hit "CTRL+C" and type something, then press enter. for a help message type "!help" and "!exit" to disconnect and exit

Commands:
-

### server:

help: this message

exit: exit the script

pass: set password

start: start the server

stop: kill the server

### client:

-h: help

### client chat commands:

!help: this message

!down: download files

!back: go back to the chat

!exit: exit the programm
