## ubuntu下使用串口工具

工具: minicom

步骤：
1. 安装。 

		sudo apt-get install minicom
2. 查看所有串口。

		cd /
        ls dev/tty*
3. 连接串口线，查看正在使用的串口。

		dmesg | grep tty // usb 3-4: pl2303 converter now attached to ttyUSB0，其中attached to xx表示目前正在使用的串口为xx。
4. 修改minicom配置。

		sudo minicom -s
        选择Serial port setup
        再按a，修改serial device值为上一步的xx串口
        按回车回到菜单页，在选择save as dfl保存设置
5. 打开串口查看日志。
 		sudo minicom 打开串口连接，ctrl+a再按x退出