#conky-Infinity-suse
专为openSUSE修改的Conky Infinity主题。

#安装说明

>一、安装：conky
     $sudo zypper in conky conky-cairo conky-imlib2

>二、将压缩包内的文件夹conky和文件conkyrc改名为.conky和.conkyrc然后将它们复制到自己的主目录下。

>三、修改.conkyrc文件中第95、96、98行中的无线网卡的名称为你的网卡名。
   
     注：我的网卡名是wlp9s0，批量替换为你的网卡名就行了。

>四、修改.conkyrc文件中第100行中的天气预报的地区编码。
   
    将 “http://weather.yahooapis.com/forecastrss?w=2172739” 中的2172739替换为你的地区编号。
    查询地区编码可到 http://weather.yahoo.com/ 输入你的城市名，如 beijing ,然后查看URL中的编号。

>五、启动
   
   1、测试启动
   
      $conky -d -c ~/.conkyrc &

   2、随桌面自动启动
      
      GNOME 桌面:
      
      在终端执行输入下面的命令,然后在调出的启动管理程序中选择[添加],[名称]可以随意填，[命令]选项中填：conky -d -q
      
      $gnome-session-properties
      
      KDE 桌面:
      
      修改~/.bash_profile文件，在里边加入下面的命令即可。如果没有这个文件就自己新建一个。
      
      conky -d -c ~/.conkyrc &

>六、修改默认图标（可选）
    
    在conky文件夹下，提供了三套天气皮肤，将自己喜欢的天气皮肤文件夹名修改为 weather 即可。