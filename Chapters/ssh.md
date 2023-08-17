# Connecting to a server

## Standard SSH connection
Use if you need to log on to the server for general tasks.

```
$ ssh <username>@<server>
```
To log in while specifying a keyfile
```
$ ssh <username>@<server> -i <path to keyfile>
```

## SSH connection with port forwarding
Useful if you need to access a remote service from your local machine. 

```
$ ssh <username>@<server> -L <localport>:localhost:<serverport>
```

For example, to forward port 3306 on the server to port 3307 on the local machine use the following command:

```
$ ssh <username>@<server> -L 3307:localhost:3306
```