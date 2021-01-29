<!-- njnmdoc: title="Hauppauge Remote for winamp"  -->

This is very old, but maybe still works? It was my most popular blog post ever.

## Config

Here’s some code for controlling Winamp with the remote that comes with a
Hauppauge TV tuner card. Since this uses the winamp API, winamp does not need
to have focus in order to receive commands. Open up
`C:\windows\irremote.ini`, and edit these lines into the [Default]
section:

```
1={FindWnd(Winamp v1.x,)}{cmd(40059)}
2={FindWnd(Winamp v1.x,)}{cmd(40040)}
3={FindWnd(Winamp v1.x,)}{cmd(40058)}
4={FindWnd(Winamp v1.x,)}{cmd(40044)}
5={FindWnd(Winamp v1.x,)}{cmd(40045)}
6={FindWnd(Winamp v1.x,)}{cmd(40048)}
7={FindWnd(Winamp v1.x,)}{cmd(40192)}
8={FindWnd(Winamp v1.x,)}{cmd(40047)}
9={FindWnd(Winamp v1.x,)}{cmd(40046)}
```


The keys are:
<ol>
<li>    Vol Down
<li>    Show Playlist
<li>    Vol Up
<li>    Prev
<li>    Play
<li>    Next
<li>    Visualization
<li>    Stop
<li>    Pause
</ol>




