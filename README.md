# peer-connect
A webrtc chat app made using peerjs. hosted [here](https://nilinswap.github.io/peer-connect/)

# Run locally
open file://<abs-path-to-project-container>/peer-connect/index.html in browser in two tabs. Open console, connect one tab to other and see them talking.


## Hooks?
1. Fix resistive connect with peer issue - sometimes even after hitting submit with a peerid there is no connect.

1.1 connect out of nat

2. Try multiple peer connect

3. how can you provision this using a single javascript?

4. How to bring in authentication

## commands

1. check what all ports are process using - 
```shell
netstat -tulpn
```

2. run turnserver manually
```shell
sudo turnserver -c /etc/turnserver.conf
```

3. manage turn server
```shell
sudo systemctl stop/start/restart coturn
```

4. check logs
```shell
   journalctl -fue coturn 
```

5. create new turn users
```shell
sudo turnadmin -a -u <username> -r <realm> -p <password>
```
in my case realm was `myturn.codes`

## Don't forget
1. `/etc/turnserver.conf` is where conf file is.
2. `/etc/default/coturn` is used to have server running from start of the server.

## Some Language

IPH - Iske Paise Hai

## Resources

1. [webrtc connectivity usecases](https://blog.addpipe.com/troubleshooting-webrtc-connection-issues/)
2. running your own coturn server in ec2. Mostly [this](https://medium.com/@omidborjian/setup-your-own-turn-stun-signal-relay-server-on-aws-ec2-78a8bfcb71c3) and also [this.](https://medium.com/swlh/setup-your-own-coturn-server-using-aws-ec2-instance-29303101e7b5)


