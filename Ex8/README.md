The code of Ex_C had a bug and it was not fully functional in practice. In the simulation (using the Arduino IDE) it was fine though. 
The ESP module couldnt receive data. The fault was the following:
The ESP module used the Jumper J17 for PD0-ESP_TX and PD1-ESP_RX connection. However PORTD was being used by the LCD by mistake at the same time. We should have used the port expander for the lcd pins. 
