 # mac 连接 xbox 手柄后会时不时的将一个手柄识别成多个，导致在游戏中同一个按键指令被响应多次
 <img src="https://github.com/Coo1things/steammatchmac/blob/main/pic/3565672506.jpg" width="50%">
 
 # 解决方式 
 
 ## 1.有时候通过重新启动 steam 和重新连接蓝牙可以解决问题，但这种方案时不时失灵
    
    * 关闭手柄：长按 xbox 手柄上的「西瓜」按钮 5 秒以上 
    * 关闭 macOS 中的蓝牙功能 
    * 退出 Steam 
    * 启动 Steam 
    * 开启手柄 
    * 打开 macOS 中的蓝牙功能 
 ## 2.此方案来自 steam 论坛，其原理是通过添加黑名单禁用 xbox-360 设备，解决方案如下

    * 启动 steam
    * 打开 steam 配置文件: ~/Library/Application Support/Steam/config/config.vdf
    * 在最后一个大括号之前添加一行代码: "controller_blacklist" "045e/028e"
    * 重启 steam
### 添加后的效果是这样的，观察下重启后的steam配置是不是类似的，如果不是，可能就是配置添加错了
    
    
    {...
    "BigPicture"
    {
        "TextInputDefaultLanguage"        "none"
        "Windowed"        "0"
    }
    "controller_blacklist"        "045e/028e"
     }
