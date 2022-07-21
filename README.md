# 0.96OLED_IIC_PCB介绍
0.96OLED_IIC_PCB是基于SSD1306和SSD1315驱动的两种0.96寸OLED屏驱动电路，仓库中包含两种驱动电路的原理图和PCB图，以及必要的原理图库、封装库和参考资料。  
以SSD1306作为驱动的OLED屏外边框较大，SSD1315则没有较多的外框玻璃，同时SSD1315供电设计更加安全稳定，在价格相近的情况下推荐优先使用SSD1315不使用~~SSD1306~~  
硬件部分的原理图与PCB均使用[Altium Designer 19](https://www.altium.com.cn/)设计和绘制
## SSD1306使用注意事项
<img src="https://github.com/EternalStarCHN/0.96OLED_IIC_PCB/blob/main/images/0.96OLED_SSD1306.PNG" width="30%" height="30%" alt="SSD1306的3D视图" position="relative" left="50%"/><br/>
使用SSD1306驱动电路的IIC输出时，只需要用 **GND**、**VCC**、**D0(SCL)**、**D1(SDA)** 四根线，因此需要注意下表中几个引脚的连接：  
| 引脚 | 连接 |
| :--- | :--- |
| BS1 | 高电平 |
| BS0 | 低电平 |
| RES | 高电平 |
| DC | 低电平 |
| CS | 低电平 |
## SSD1315使用注意事项
<img src="https://github.com/EternalStarCHN/0.96OLED_IIC_PCB/blob/main/images/0.96OLED_SSD1315.PNG" width="30%" height="30%" alt="SSD1315的3D视图"/><br/> 
通过改变D/C#脚接4.7K电阻后是接VCC还是接GND，可以改变IIC的地址：  
| IIC | VCC | GND |
| :--- | :---: | :---: |
| 0x78 | × | √ |
| 0x76 | √ | × |
(√表示接4.7K电阻后连接，×表示不连接)
# 许可证
0.96OLED_IIC_PCB is licensed under [GNU General Public License v3.0](https://github.com/EternalStarCHN/0.96OLED_IIC_PCB/blob/main/LICENSE).
