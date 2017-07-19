+++

date = "2017-07-17T21:38:44+08:00"

title = "a glimpse at Bluetooth mesh"

categories = [  "BLE",]

Tags = ["BLE", "MESH"]

+++






------

今日蓝牙SIG发布了Mesh相关技术，在其昨日发表的博文中这样说到：

> Bluetooth mesh networking is the most robust and powerful low-power radio technology for connected lighting in commercial spaces, and it is the change the lighting industry has been waiting for,
> We're excited the world will finally see the efforts and contributions of Silvair and all the other dedicated working group member companies - the Bluetooth mesh revolution has officially started.

同日,BLE领域的领头羊Nordic也在市场上推出了其基于mesh的nRF5软件开发套件（标准制定优势啊！！！）。

SIG在其相关博文中提到

>Bluetooth mesh networking utilizes a managed flood approach for message transmission, which is a simple and reliable form of message relay that is uniquely suited for low-power wireless mesh networks, especially those handling a significant amount of multicast traffic.

从这段话中可以窥得一二，mesh的转发机制采用了简单可控的message flood，在没看spec的情况下大胆猜测下，这种转发机制应该还是类似于广播，应该不是连接，毕竟维持多链接在底层应该比较痛苦，也不适合它所说的low-power应用。如果采用类似广播的机制的话，可以达到实现简单，可拓展性强的特点。另外，应该不会采用zigbee中类似路由表的方式，毕竟那个也不能称之为简单，毕竟是“a managed flood approach”,lol!

SIG官方对mesh的定位也很清晰，继续引文~~

>Bluetooth mesh networking is poised to further catalyze beacons, robotics, industrial automation, energy management, smart city applications, and other industrial IoT and advanced manufacturing solutions.

话都被说绝了，zigbee还搞毛啊！！


# 下面看看mesh的spec吧

### [Mesh Networking Specifications](https://www.bluetooth.com/specifications/mesh-specifications)
打开链接以后可以看到spec分为三部分，分别是

> * Mesh Profile: Defines fundamental requirements to enable an interoperable mesh networking solution for Bluetooth LE wireless technology
> * Mesh Model: Introduces models, used to define basic functionality of nodes on a mesh network
> * Mesh Device Properties: Defines device properties required for the Mesh Model specification

其实打开链接的头部也比较清晰的显示了一条信息，说明此次的Mesh技术是针对BLE的，而不是有些谣传的双模的或者远古就存在的Mesh。

>The Bluetooth® mesh networking specifications define requirements to enable an interoperable many-to-many (m:m) mesh networking solution for Bluetooth Low Energy (LE) wireless technology

好久不用markdown，手有点生硬，关于spec内容介绍下次再讲。

谢谢！！

edited with Cmd Markdown by ghosert

