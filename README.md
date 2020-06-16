# Procedure for Raspberry Pi 3+ headless setup to run ROS nodes over Docker

## This procedure is based on [PiBackery 0.3.8](https://github.com/davidferguson/pibakery/releases/tag/v0.3.8) and [Raspbian Lite](https://www.raspberrypi.org/downloads/raspberry-pi-os/) image

- Create a partition on an SD card formatted in exFat
- Install _PiBackery_ with _Raspbian Lite_ only (don't accept updates as newer _Setup WiFi_ block is broken)
- Run _PiBackery_ and import _HeadlessSetup.xml_
- Fill in fields with hostname and WiFi settings and then write the image

> Run SSH client to connect using the hostname you have filled in, default user _pi_ and its password _raspberry_.   
> It may take 5-10 minutes on the first launch before SSH client can connect.  

---

Now you can connect [CSI interface camera](https://projects.raspberrypi.org/en/projects/getting-started-with-picamera) and run [docker-picamera](https://github.com/pschmitt/docker-picamera/blob/master/Dockerfile) image by entering the following command:  
> `docker run --rm -it -p 8000:8000 --device=/dev/vchiq pschmitt/picamera`