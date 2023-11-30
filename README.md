# ECE-4180-Final-Project

## Wiring

### Bluetooth

| Bluetooth | MOD | CTS | TXO | RXI | VIN        | RTS | GND | DFU |
|-----     |-----|-----|-----|-----|-----       |-----|-----|-----|
|  Mbed    |     | GND | P14 | P13 | 5V external|     | GND |     |

### Rain drop detector (MH sensor)

| MH Sensor| AO  | DO  | GND | Vcc |
|-----     |-----|-----|-----|-----|
|  Mbed    | P20 | P5  | GND | VIN |

### uLCD

|uLCD| 5V         | RX  | TX | GND | RES |
|----|-----       |-----|----|-----|-----|
|Mbed| 5V external| P10 | P9 | GND | P11 |

### DHT11

|DHT11| +   | OUT | -  |
|---- |-----|-----|----|
|Mbed | VIN | P23 |GND |

### Sonar

|Sonar| Vcc       | Trig | Echo| GND|
|---- |-----      |----- |---- |----|
|Mbed |5V external| P6   |  P7 | GND|

### IMU

|IMU  | SCL | SDA | UDO| GND|
|---- |-----|-----|----|----|
|Mbed | P27 | P28 | VIN| GND|

### Motor

|Motor|C  | +  | -  |
|---  |---|--- |--- |
|Mbed |P21| P27| GND|


### Speaker

![speaker wiring](speaker.png)

|R1 |Vout or Vu |
|---|---        |
|P24|5V external|


