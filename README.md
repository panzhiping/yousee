* 1.请自己安装ffpmeg跟nginx（我的ffmpeg是3.4.4，nginx是1.14.0）
* 2.nginx.conf中的location下的路径，请改成你自己电脑上的路径。
* 3.media目录下，我放了2个脚本。
  * 1）convert.sh是用来将MP4跟flv文件， 转成小分辨率（192x144）跟大分辨率（640x480)，并截图。
 其中小分辨率（192x144）即为用来预览的视频。
  * 2）json.sh用来根据目录下的文件名，生成文件列表的json数据，其中SERVER要跟你得nginx的IP跟监听端口一致。
  * 3）使用json.sh生成list.data后，放到你的dist目录下即可。
* 4.backend和nginx/mempipe，实现了nginx与后端程序的交互， backend主要是根据nginx传过来的id动态生成html，返回给nginx
* 5.我用的react来绘制组件，要更改页面样式的，可以去webpack目录里修改对应文件
![image](https://github.com/yechaoqun/yousee/blob/master/image.gif) 
