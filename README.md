# av-loopback
Androud kernel video(v4l2) and audio(alsa) loopback driver.

基于v4l2和alsa实现的回环虚拟驱动，可同时创建任意参数的多个虚拟摄像头和声卡设备，支持一端写入数据到虚拟设备驱动，同时另一端从虚拟设备驱动读取数据。
例如：用于Android系统不同进程间的音视频数据传输。