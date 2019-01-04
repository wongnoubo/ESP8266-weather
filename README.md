
# stm32控制ESP8266获取天气api并且在led屏幕上显示

------
**使用：** 
> * 在ATK_ESP8266文件夹下面的wifista.c第14行修改wifi的ssid号和密码。编译烧录后即可使用。
> * 在ATK_ESP8266文件夹下面的weather.c中修改85行修改天气api。
> * 在PICTURE文件夹下面的picture.c修改led显示的背景图片。
> * 时间的显示可以使用stm32的实时时钟模块，然后串口授时；使用时间API获取北京时间。 


**实验器材：**
> * 战舰V3\精英STM32F103开发板
> * ESP8266wifi模块
	
**实验目的：**
> * 学习ATK_ESP8266高性能UART_WIFI模块的使用,掌握基本的TCP，UDP通信串口AT指令配置方法.
> * 获取天气api,获得天气并且显示。

**硬件资源：**
	1,DS0(连接在PB5)
	2,串口1(波特率:115200,PA9/PA10连接在板载USB转串口芯片CH340上面)
	3,串口3(波特率:115200，PB10/PB11)
	4,ALIENTEK 2.8/3.5/4.3/7寸TFTLCD模块(通过FSMC驱动,FSMC_NE4接LCD片选/A10接RS)
	5,按键KEY0(PE4)/KEY1(PE3)/KEY_UP(PA0,也称之为WK_UP)
	6,SD卡,通过SDIO(SDIO_D0~D4(PC8~PC11),SDIO_SCK(PC12),SDIO_CMD(PD2))连接 
	7,W25Q128(SPI FLASH芯片,连接在SPI2上)
	8,24C02
	9,ATK_ESP8266 WIFI模块1个
	10.3.5寸LCD屏幕
	
**连接方式：**
	模块与带有无线网卡的电脑或其他wifi设备连接：采用wifi连接
	模块与开发板连接（TTL串口方式）：
	ATK-ESP8266 WIFI模块与精英板连接方式（通过4根杜邦线连接）：
	ATK-ESP8266 WIFI模块    战舰V3\精英STM32开发板
	   TXD<------------>PB11
	   RXD<------------>PB10
	   GND<------------>GND
	   VCC<------------>3.3V\5V
		
**实验现象:**
	通过api获取网络天气并且图文并茂显示，led上可以显示北京时间。
	

	




































































