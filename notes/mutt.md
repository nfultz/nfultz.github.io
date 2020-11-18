<!-- njnmdoc:  title="Ad Blocking"  -->

<blockquote>"All mail clients suck. This one just sucks less."</blockquote><cite>Mutt Homepage</cite>

mutt is a no-frills email client for the terminal.

The default build assumes you are using a MTA / MDA (traditional UNIX setup). To build with IMAP / POP / SMTP support,
use:

```
./configure --enable-imap --enable-smtp --with-ssl
```

## Using with MS Exchange
One solution is to set up DavMail, which will proxy Exchange. It works but it's slow.

```
#Assumming davmail is running locally
mailboxes imap://nfultz@localhost:49156/
set smtp_url = smtp://nfultz@localhost:49153
set from = nfultz@Mega.corp
```

<h2 id=gmail> Using with Gmail </h2>

Gmail is easy enough to set up since it supports IMAP.

However, be careful when you google for mutt config tips, a lot of info is out of date.

Since 2014, google has been
[ramping up security](http://googleonlinesecurity.blogspot.co.uk/2014/04/new-security-measures-will-affect-older.html),
which includes disabling password logins via IMAP and POP.

If you are an admin, you can reenable password logins on the [less secure apps settings](https://myaccount.google.com/lesssecureapps).

The recommended approach is to create a "secure app" which authenticates using OAuth2. This is a bit involved:

1. Create a new project on the [Google Developer Console](https://console.developers.google.com/)
2. Create a "OAuth 2.0 Client ID"

Then you need to get the actual token:

1.  copy `src/contrib/mutt_oauth2.py`
  * edit encrypt / decrypt pipeline
  * edit client id and secret (from google developer console)
  * chmod +x
2. `mutt_oauth2.py .cache/mutt_token --verbose --authorize`
3  `mutt_oauth2.py .cache/mutt_token --verbose --test`


Finally, update your `.muttrc` to use the new features:

```
set imap_authenticators="oauthbearer:xoauth2"
set imap_oauth_refresh_command="mutt_oauth2.py ~/.cache/mutt_token"
set smtp_authenticators=${imap_authenticators}
set smtp_oauth_refresh_command=${imap_oauth_refresh_command}
```

