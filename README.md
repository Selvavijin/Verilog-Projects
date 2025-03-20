# Verilog-Projects

Serial Peripheral Interface(SPI)  

It is a serial communication protocol and is developed by motorola. It is used to send data between microcontrollers and peripherals like EEPROM, SD CARD, RTC, DAC any many more. It has the maximum speed of over 10 Mbps. It is a synchronized data bus.   
Inside the Mobile, we have microprocessors and other modules like Camera. Here, if the microprocessor has to send data to the camera module, then the microprocessor is the master and the camera is the slave. This communication is done using SPI bus.  
Easy interface - To transfer data through the internet, we use Ethernet which uses many signal lines(Eg: 100 signal lines) for communication. But, this SPI uses only 4 wires. So, ethernet occupies more space and the SPI requires less hardware. 
4 wires -> 1.SCLK - serial clock - Used for all data communication.  
2.MOSI - Master out Slave in.  
3.MISO - Master in Slave out.
4.SS/CS - Slave select/ Chip Select.  
SPI is a full duplex which means that the master and slave can transfer data at the same time using MOSI and MISO. 
SCLK,CS,MOSI is always produced by the master.  
In our case, since we are going with verilog code, the master is FPGA and the slave is any sensors.   
->SPI protocol is normally used for short distance communication(Between the same circuit board or between the devices of the same PCB). Eg: Inside the mother board, let us say that we have Microprocessor and ADC. So both can be communicated using the SPI, if it supports.  
->It supports single master. All other devices are slaves.  
->For every slave, there is a SS(slave select) line, whcih occupies space when more slaves are added. It is a disadvantage.  
->It is preferable where large amount of high speed data is  not transferred.  
->Here the advantage is, any number of bit can be sent or received in a continuous stream. Whereas, other protocols has fixed data rate.

![image](https://github.com/user-attachments/assets/37514db7-af01-49bb-b774-f68992c04903)

