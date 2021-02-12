# USB_camera_stream
USB camera streaming Project

## Getting Started

This instructions will help you to stream USB camera video frames data on local host.

### Prerequisites

Linux (>= 14.04)
mplayer utility
nc utility

### Instruction
```

--> Compile the source code and use following command to send video frames over local host.

    ./capture_video -d /dev/<VIDEO_NODE> -o | nc 127.0.0.1 5555

--> Create one fifo to grab the data from local network.

    nc -l -p 5555 > video.fifo

--> Play fifo data by passing the following arguments to mplayer.

    mplayer video.fifo -demuxer rawvideo -rawvideo w=640:h=480:format=yuy2

```


## Authors

* **Nueral Space** 
