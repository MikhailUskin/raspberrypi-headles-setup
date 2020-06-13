# Docker ready headless setup procedure for Raspberry Pi 3+

## This procedure is based on [PiBackery 0.3.8](https://github.com/davidferguson/pibakery/releases/tag/v0.3.8) and RaspbianLite image

- Create a partition on an SD card and format it in exFat
- Install PiBackery with 'Raspbian Lite' only (*don't accept updates as newer 'Setup WiFi' block is broken*)
- Run PiBackery and import 'HeadlessSetup.xml'
- Fill in fields with hostname and WiFi settings then write the image

---

*Run SSH client to connect using the hostname you have filled in, default user 'pi' and its password 'raspberry'*.   
*It may take 5-10 minutes on the first launch before SSH client can connect*.  
