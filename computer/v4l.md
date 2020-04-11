## Video 4 Linux

### OBS

### Dumping OBS video to Zoom

https://github.com/CatxFish/obs-v4l2sink

deb here https://github.com/CatxFish/obs-v4l2sink/releases

Video Only for now

- To play audio, go through analog hole (eg mic is not too far from speakers)

See https://github.com/CatxFish/obs-v4l2sink/issues/17#issuecomment-603125325 to install module from source


https://obsproject.com/forum/threads/has-anyone-successfully-output-from-obs-to-a-live-zoom-conference-on-linux.117026/#post-444361

for ubuntu config



### Bridging audio

    $pacmd load-module module-virtual-source source_name=VirtualMic
    $pacmd load-module module-null-sink sink_name=MySink


In OBS - audio advanced properties - turn on monitor for sources
Then in pavucontrol, playback tab - change all obs monitors to null output
pavucontrol recording tab - change virtualmic to monitor of null output

zoom - audio - use virtual mic

Note that this is laggy as hell.

Cleanup:

    $pacmd list-modules
    $pacmd unload-module 35
    $pacmd unload-module 36


