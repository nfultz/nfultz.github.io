<!-- njnmdoc:  title="Utils"  -->

# Abduco + dvtm

Seems like a promising [[suckless]] alternative to [[screen]].

[abduco main site](http://www.brain-dump.org/projects/abduco/)

[dvtm main site](http://www.brain-dump.org/projects/dvtm/)

# bitlbee

bitlbee is an IRC-to-chat bridge; it lets you use AIM, gTalk, etc through a standard IRC client.

To get started, send bitlbee

help quickstart

and follow the directions.

For gTalk, you need to add a jabber account. If the account is a hosted Google  and then reset the server.

[Bug 1179](http://bugs.bitlbee.org/bitlbee/ticket/1179) explains a workaround if the gTalk connection is flaky.

<h1 id=ssh_key_encrypt>Quick encryption</h1>

If you have someone's ssh public key, and need to send them a small message (eg password)

Note need to convert pubkey to PKCS8 format for compatibility with openssl rasutl

```
ssh-keygen -e -f $HOME/.ssh/id_rsa.pub -m PKCS8 > ~/.ssh/id_rsa.pem.pub
openssl rsautl -raw -pubin -inkey /home/nfultz/.ssh/id_rsa.pem.pub  -in foo >foo.enc
openssl rsautl -decrypt -raw -inkey ~/.ssh/id_rsa -in foo.enc -out -
```

# REPL tools

sudo gem install repl

sudo apt-get install rlwrap

To make a git repl:

$ repl git

Add readline capabilities to [[sic]]

$ rlwrap sic -h localhost


# Misc

https://github.com/jarun/nnn
https://dev.yorhel.nl/ncdu
