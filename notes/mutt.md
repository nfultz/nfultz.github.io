<blockquote>"All mail clients suck. This one just sucks less."</blockquote><cite>Mutt Homepage</cite>

mutt is a no-frills, [[suckless]] email client for the terminal.

One solution is to set up [[DavMail]], which will proxy exchange. It works but it's slow.

#Assumming davmail is running locally

mailboxes imap://nfultz@localhost:49156/

set smtp_url = smtp://nfultz@localhost:49153

set from = nfultz@Mega.corp

Gmail is easy enough to set up since it supports IMAP. However, be careful when you google for mutt config tips, a lot of info is out of date.

mailboxes imaps://nfultz@imap.gmail.com/

set smtp_url = smtps://nfultz@smtp.gmail.com

set from = nfultz@gmail.com

Google appears to be [ramping up security](http://googleonlinesecurity.blogspot.co.uk/2014/04/new-security-measures-will-affect-older.html), which breaks the config above.

To fix it, we will have to set up OAuth using [SASL-XOAuth](https://github.com/simmel/saslxoauth).

First, you will have to generate a token:

$ wget http://google-mail-xoauth-tools.googlecode.com/svn/trunk/python/xoauth.py

$ python xoauth.py --generate_oauth_token --user=nfultz@gmail.com



Copy and paste the token info into <code>~/.xoauthrc</code>

You may also need to install libsasl2-dev and liboauth-dev

Then download and install the XOAuth library from github:

$ git clone https://github.com/simmel/saslxoauth.git

$ cd saslxoauth

$ make

$ checkinstall

$ sudo dpkg -i *.deb

Finally, set the auth measure in mutt's config:

set imap_authenticators="XOAUTH"

set smtp_authenticators="XOAUTH"

On SUSE, you may need to install to <code>/usr/lib64</code> instead of <code>/usr/lib</code>

