# The Smart Hat

**Team members: Joseph Ferraro, Phat Bui, Pengyu Mo, Xueqing Li**

**Georgia Institute of Technology**

## Table of Content
* [Project Description](#project-description)
* [Technical Specification](#technical-specification)
* [Part Lists](#parts-list)
* [Schematic and Connection Guide](#schematic-and-connection-guide)
* [Source Code](#source-code)
* [Future Plan](#future-plan)

## Project Description

We want to develop a smart hat designed to integrate a range of Internet of Things (IoT) functionalities. This hat features an ultra-thin LCD (uLCD) screen on the brim for displaying information. To ensure the wearer is prepared for various weather conditions, we have included a temperature sensor and a rain detection sensor. Additionally, a speaker is incorporated to emit sounds, particularly useful when the rain sensor activates, indicating conditions where wearing the device might be unsuitable. For navigation and orientation assistance, an inertial measurement unit (IMU) tracks the wearer's movement and direction. On the side of the hat, there is a fan that activates to provide cooling when needed. All these functionalities are Bluetooth-enabled, allowing for convenient control and management through a phone or other device. Our design aims to create a hat that easily integrates into daily life while offering high functionality and convenience.

Project Video: [![Project Video]([https://img.youtube.com/vi/VIDEO_ID/0.jpg](https://youtu.be/hd9vFIxSbDE))]([https://www.youtube.com/watch?v=VIDEO_ID](https://youtu.be/hd9vFIxSbDE))

<p align="center">
  <img src="https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/Wearing.jpg" alt="Wearing" width="70%">
</p>

*<p align="center">The Smart Hat Prototype</p>*

The uLCD display in the Smart Hat will feature four pages, each presenting information on different functionalities. The wearer can easily switch between pages by waving their hand over the sensor located on the side of the hat. The images below illustrate each page:

The images below illustrate each page:

<p align="center">
  <img src="https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/Page_1.jpg" alt="Page 1" width="50%">
</p>
<p align="center"><em>Page 1: Show The Time, Temperature Degrees in °C and °F, And Percent Humidity</em></p>

<p align="center">
  <img src="https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/page_2.jpg" alt="Page 2" width="50%">
</p>
<p align="center"><em>Page 2: Display The Orientation Of The Hat, Similar To A Compass</em></p>

<p align="center">
  <img src="https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/Page_3.jpg" alt="Page 3" width="50%">
</p>
<p align="center"><em>Page 3: Display The To-Do List</em></p>

<p align="center">
  <img src="https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/page_4.jpg" alt="Page 4" width="50%">
</p>
<p align="center"><em>Page 4: Display The Number Of Steps Taken</em></p>

## Technical Specification

The Smart Hat is controlled by the Mbed LPC1768 microcontroller. Connected to the Mbed are several components: multiple sensors, an uLCD display, a Bluetooth module, a speaker, and a motor. We have selected these parts for their common usage in many Internet of Things (IoT) devices, ensuring accessibility and compatibility. The code necessary to operate the Mbed in this project is available on the wiki page [Source Code](#source-code).

![image](https://github.com/Pengyu-Mo/ECE-4180-Final-Project/assets/117612624/e711c8c6-cf09-4180-b372-8fe0e73b6848)
*<p align="center">The Smart Hat Block Diagram</p>*

## Parts List

**Electronics:**

* [Mbed](https://www.sparkfun.com/products/9564)
* [Bluetooth](https://www.adafruit.com/product/2479)
* [MH sensor](https://www.amazon.com/Uxcell-a13082300ux1431-Rainwater-Detection-3-3V-5V/dp/B00GN7O7JE/ref=asc_df_B00GN7O7JE/?tag=hyprod-20&linkCode=df0&hvadid=652600016786&hvpos=&hvnetw=g&hvrand=3049316794955189760&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9010813&hvtargid=pla-442799778878&psc=1&mcid=b8af0bc67069391fb5206a7026de430d)
* [uLCD Display](https://www.sparkfun.com/products/11377)
* [DHT11](https://components101.com/sensors/dht11-temperature-sensor)
* [Sonar](https://www.sparkfun.com/products/15569)
* [IMU](https://os.mbed.com/components/LSM9DS1-IMU/)
* [DC Motor And Fan Blade](https://www.aliexpress.us/item/3256801919556413.html?src=google&src=google&albch=shopping&acnt=708-803-3821&slnk=&plac=&mtctp=&albbt=Google_7_shopping&albagn=888888&isSmbAutoCall=false&needSmbHouyi=false&albcp=19623912707&albag=&trgt=&crea=en3256801919556413&netw=x&device=c&albpg=&albpd=en3256801919556413&gad_source=1&gclid=CjwKCAiA98WrBhAYEiwA2WvhOgT-FWgaJjBMGs5_TeKfunDBgLqW-YByVRNVgoUzCFIs9HU_k5XgNxoC3YYQAvD_BwE&gclsrc=aw.ds&aff_fcid=9804387b83e4424580969e41ff19a63c-1701981776146-07495-UneMJZVf&aff_fsk=UneMJZVf&aff_platform=aaf&sk=UneMJZVf&aff_trace_key=9804387b83e4424580969e41ff19a63c-1701981776146-07495-UneMJZVf&terminal_id=914cdf74d6e445cdb004d445b2f34ed6&afSmartRedirect=y&gatewayAdapt=glo2usa)
* [Speaker](https://www.sparkfun.com/products/11089)
* [MOSFET](https://www.sparkfun.com/products/retired/12959)
* [Battery Pack](https://www.sparkfun.com/products/9835)

**Non Electronics:**

* Black Hat

## Schematic and Connection Guide

Here is a picture of our fully assembled hat.

<p align="center">
  <img src="https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/Hat.jpg" alt="Hat" width="80%">
</p>

*<p align="center">The Smart Hat Assembled</p>*

**Connection Tables**

Bluetooth: Adafruit Bluefruit LE UART Friend - Bluetooth Low Energy (BLE)

| Bluetooth | MOD | CTS | TXO | RXI | VIN        | RTS | GND | DFU |
|-----     |-----|-----|-----|-----|-----       |-----|-----|-----|
|  Mbed    |     | GND | P14 | P13 | 5V external|     | GND |     |

Raindrop detector (MH sensor)

| MH Sensor| AO  | DO  | GND | Vcc |
|-----     |-----|-----|-----|-----|
|  Mbed    | P20 | P5  | GND | VIN |

uLCD: Serial Miniature LCD Module - 1.44" (uLCD-144-G2 GFX)

|uLCD| 5V         | RX  | TX | GND | RES |
|----|-----       |-----|----|-----|-----|
|Mbed| 5V external| P10 | P9 | GND | P11 |

DHT11 - Temperature and Humidity Sensor

|DHT11| +   | OUT | -  |
|---- |-----|-----|----|
|Mbed | VIN | P23 |GND |

Sonar: Ultrasonic Distance Sensor - HC-SR04 (5V)

|Sonar| Vcc       | Trig | Echo| GND|
|---- |-----      |----- |---- |----|
|Mbed |5V external| P6   |  P7 | GND|

IMU: LSM9DS1 IMU

|IMU  | SCL | SDA | UDO| GND|
|---- |-----|-----|----|----|
|Mbed | P27 | P28 | VIN| GND|

Motor

|Motor|C  | +  | -  |
|---  |---|--- |--- |
|Mbed |P21| P27| GND|


Speaker - PCB mount

![speaker](https://github.com/Pengyu-Mo/ECE-4180-Final-Project/blob/main/speaker.png)

||R1 |Vout or Vu |
|--|---|---        |
|Mbed |P24|5V external|

## Source Code

~~~
#include "mbed.h"
#include "rtos.h"
#include "uLCD_4DGL.h"
#include "LSM9DS1.h"
#include "XNucleo53L0A1.h"
#include "DHT.h"
#include "Speaker.h"
#include <stdio.h>
#include "ultrasonic.h"


uLCD_4DGL uLCD(p9,p10,p11);

DigitalIn DO(p5);
AnalogIn AO(p20);

Speaker mySpeaker(p24);
RawSerial blue(p13,p14);
PwmOut mot(p21);

Serial pc(USBTX, USBRX);

DigitalOut shdn(p26);
// This VL53L0X board test application performs a range measurement in polling mode
// Use 3.3(Vout) for Vin, p28 for SDA, p27 for SCL, P26 for shdn on mbed LPC1768

//I2C sensor pins
//#define VL53L0_I2C_SDA   p28
//#define VL53L0_I2C_SCL   p27

static XNucleo53L0A1 *board=NULL;

DHT sensor(p23,SEN11301P); // Use the SEN11301P sensor

Ticker rain_indicator;

// mutex to make the lcd lib thread safe
Mutex lcd_mutex;
volatile int clear = 0;
volatile int draw = 1;
volatile int draw_c = 0;
volatile int draw_b = 0;
volatile int draw_p = 0;
volatile int ready = 0;
volatile int steps = 0;
volatile int fan = 0;
volatile float heading = 0.0;

void dist(int distance)
{
    //pc.printf("D=%ld mm  draw=%d   draw_c=%d\r\n", distance, draw, draw_c);
    if(ready && distance > 50 && distance < 100){
        lcd_mutex.lock();
        uLCD.cls();
        lcd_mutex.unlock();
        if(draw){
            draw = !draw;
            draw_c = !draw_c;
        }else if(draw_c){
            draw_c = !draw_c;
            draw_b = !draw_b;
        }else if(draw_b){
            draw_b = !draw_b;
            draw_p = !draw_p;
        }else if(draw_p){
            draw_p = !draw_p;
            draw = !draw;
        }
        lcd_mutex.lock();
        uLCD.cls();
        lcd_mutex.unlock();
        Thread::wait(1000);
    }
}

ultrasonic mu(p6, p7, .1, 1, &dist);    //Set the trigger pin to D8 and the echo pin to D9
                                        //have updates every .1 seconds and a timeout after 1
                                        //second, and call dist when the distance changes
                                    
LSM9DS1 IMU(p28, p27, 0xD6, 0x3C);

#define DECLINATION -4.94 // Declination (degrees) in Atlanta,GA.
#define PI 3.1415926

// Thread 1
void thread1(void const *args)
{
    float prev_temp_C = 999.0;
    float prev_temp_F = 999.0;
    float prev_humi = 999.0;

    int err;
    while (1) {
        err = sensor.readData();
        //pc.printf("err: %d draw: %d \r\n", err, draw);
        if(ready){
            lcd_mutex.lock();
            uLCD.filled_rectangle(31, 0, 62, 5, 0xff6666);
            uLCD.filled_rectangle(95, 0, 127, 5, 0xffff66);
            lcd_mutex.unlock();
        }

        if (ready && draw) {
            pc.printf("err: %d\n\r", err);
            if(err == 0){
                if(sensor.ReadTemperature(CELCIUS) != prev_temp_C
                    || sensor.ReadTemperature(FARENHEIT) != prev_temp_F
                    || sensor.ReadHumidity() != prev_humi){
                    prev_temp_C = sensor.ReadTemperature(CELCIUS);
                    prev_temp_F = sensor.ReadTemperature(FARENHEIT);
                    prev_humi = sensor.ReadHumidity();
                }
            }
            
            if(prev_temp_C == 999.0){
                lcd_mutex.lock();
                uLCD.set_font(FONT_7X8);
                uLCD.text_width(2);
                uLCD.text_height(2);

                uLCD.locate(0,5);
                uLCD.color(GREEN);
                uLCD.printf("... C \r\n");

                uLCD.locate(0,6);
                uLCD.color(RED);
                uLCD.printf("... F \r\n");

                uLCD.locate(0,7);
                uLCD.color(WHITE);
                uLCD.printf("... %% \r\n");
                lcd_mutex.unlock();
            }else{
                lcd_mutex.lock();
                uLCD.set_font(FONT_7X8);
                uLCD.text_width(2);
                uLCD.text_height(2);

                uLCD.locate(0,5);
                uLCD.color(GREEN);
                uLCD.printf("%3.1f C \r\n", prev_temp_C);

                uLCD.locate(0,6);
                uLCD.color(RED);
                uLCD.printf("%3.1f F \r\n", prev_temp_F);
                //uLCD.printf("Temperature is %4.2f K \r\n",sensor.ReadTemperature(KELVIN));
                uLCD.locate(0,7);
                uLCD.color(WHITE);
                uLCD.printf("%3.1f %% \r\n", prev_humi);
                lcd_mutex.unlock();
                //uLCD.printf("Dew point is %4.2f  \r\n",sensor.CalcdewPoint(sensor.ReadTemperature(CELCIUS), sensor.ReadHumidity()));
                //uLCD.printf("Dew point (fast) is %4.2f  \r\n",sensor.CalcdewPointFast(sensor.ReadTemperature(CELCIUS), sensor.ReadHumidity()));
            }
        } 
        
        if(ready && draw_c){
            lcd_mutex.lock();
            uLCD.filled_rectangle(31, 0, 62, 15, RED);
            lcd_mutex.unlock();

            // mx = -mx;
            // // Adjust the heading calculation to point to South
            // if (my == 0.0)
            //     heading = (mx < 0.0) ? 0.0 : 180.0; // If pointing to North, make it South
            // else
            //     heading = atan2(mx, my) * 360.0 / (2.0 * PI);

            // // Adjust for magnetic declination. Since you want to point to South, 
            // // you need to add 180 degrees to the declination
            // heading += DECLINATION + 180.0;

            // // Normalize the heading to be between 0 and 360
            // heading = fmod(heading, 360.0f);
            // if (heading < 0) heading += 360.0;

            int centerX = 64;
            int centerY = 64;
            float arrowLength = 30.0;  // Length of the arrow shaft

            // Convert heading to radians
            float radianHeading = (-heading * PI / 180.0);

            // Calculate arrow tip (head) coordinates
            float xTip = centerX + arrowLength * sinf(radianHeading);
            float yTip = centerY + arrowLength * cosf(radianHeading);

            lcd_mutex.lock();
            //uLCD.filled_rectangle(, , , , 0x00FF00);
            // Drawing the arrow shaft
            uLCD.line(centerX, centerY, xTip, yTip, 0xFFFFFF);
            Thread::wait(200);
            uLCD.line(centerX, centerY, xTip, yTip, 0x000000);
            lcd_mutex.unlock();
        }

        if(ready && draw_p){
            lcd_mutex.lock();
            uLCD.filled_rectangle(95, 0, 127, 15, 0xffff00);
            uLCD.color(WHITE);
            uLCD.text_height(2);
            uLCD.text_width(2);
            uLCD.set_font(FONT_7X8);
            uLCD.locate(4,4);
            uLCD.printf("%d", steps);
            lcd_mutex.unlock();
        }
        Thread::wait(300);
    }
}

// Thread 2
void thread2(void const *args)
{
    //blue.baud(9600);
    //blue.attach(&dev_recv, Serial::RxIrq);
    char str[200] = {};
    int run = 1;
    int line = 0;
    int col = 2;
    char bnum=0;
    
    while(1) {
        if(ready){
            lcd_mutex.lock();
            uLCD.filled_rectangle(63, 0, 94, 5, 0x6666ff);
            lcd_mutex.unlock();
        }
        
        if(ready && !draw_b){
            while(blue.readable()) {
                char c = blue.getc();
                if (c =='!') {
                    if (blue.readable() && blue.getc()=='B') { //button data
                        if(blue.readable()){
                            bnum = blue.getc(); //button number
                        }

                        if ((bnum>='1')&&(bnum<='4')){
                            if(bnum == '3'){
                                fan = 1;
                                break;
                            }else if(bnum == '4'){
                                fan = 0;
                                break;
                            }
                        }
                    }else{
                    }
                }else{
                }
            }
        }

        if(ready && draw_b){
            lcd_mutex.lock();
            uLCD.filled_rectangle(63, 0, 94, 15, BLUE);
            uLCD.locate(0, 2);
            lcd_mutex.unlock();

            if(!run){
                for (int i = 0; str[i] != '\0'; i++) {
                    lcd_mutex.lock();
                    uLCD.putc(str[i]);
                    lcd_mutex.unlock();
                }
                run = 1;
            }

            lcd_mutex.lock();
            uLCD.locate(0, col);
            lcd_mutex.unlock();

            while(blue.readable()) {
                char c = blue.getc();
                if (c =='!') {
                    if (blue.readable() && blue.getc()=='B') { //button data
                        if(blue.readable()){
                            bnum = blue.getc(); //button number
                        }

                        if ((bnum>='1')&&(bnum<='4')){
                            if(bnum == '1'){
                                clear = 1;
                                break;
                            }else if(bnum == '2'){
                                clear = 0;
                                break;
                            }else if(bnum == '3'){
                                fan = 1;
                                blue.getc();
                                blue.getc();
                                break;
                            }else if(bnum == '4'){
                                fan = 0;
                                blue.getc();
                                blue.getc();
                                break;
                            }
                        }
                    }else{
                        lcd_mutex.lock();
                        uLCD.putc(c);
                        lcd_mutex.unlock();
                    }
                }else{
                    lcd_mutex.lock();
                    uLCD.putc(c);
                    lcd_mutex.unlock();
                }

                int len = strlen(str);   // Get the current length of the string
                if (len < sizeof(str) - 1) {
                    str[len] = c;       // Add the character at the end
                    str[len + 1] = '\0'; // Null-terminate the string
                }
                line = 1;
            }

            if(line){
                col++;
                line = 0;
            }
            
            // Clear the string when draw_b transitions from 0 to 1
            if (clear) {
                col = 2;
                clear = 0;
                memset(str, 0, sizeof(str)); // Clear the string
                lcd_mutex.lock();
                uLCD.cls();
                lcd_mutex.unlock();
                while(blue.readable()) {
                    char c = blue.getc();
                }
            }
        }else{
            run = 0;
        }
        Thread::wait(300);
    }
}


void thread3(void const *args)
{
    IMU.begin();
    if (!IMU.begin()) {
        pc.printf("Failed to communicate with LSM9DS1.\n");
    }
    IMU.calibrate(1);
    IMU.calibrateMag(0);
    ready = 1;

    int sample_num = 1;
    float mag = 0;
    float buffer[2] = {0};
    float avg_buffer[2] = {0};
    float avg;
    lcd_mutex.lock();
    uLCD.cls();
    lcd_mutex.unlock();
    while(1) {
        while(!IMU.magAvailable(X_AXIS));
        IMU.readMag();
        float mx = IMU.calcMag(IMU.mx);
        float my = IMU.calcMag(IMU.my);
        float mz = IMU.calcMag(IMU.mz);
        while(!IMU.accelAvailable());
        IMU.readAccel();
        float ax = IMU.calcMag(IMU.ax);
        float ay = IMU.calcMag(IMU.ay);
        float az = IMU.calcMag(IMU.az);

        // touchy trig stuff to use arctan to get compass heading (scale is 0..360)
        mx = -mx;
        if (my == 0.0)
            heading = (mx < 0.0) ? 180.0 : 0.0;
        else
             heading = atan2(mx, my)*360.0/(2.0*PI);
        //pc.printf("heading atan=%f \n\r",heading);
        heading -= DECLINATION; //correct for geo location
        if(heading>180.0) heading = heading - 360.0;
        else if(heading<-180.0) heading = 360.0 + heading;
        else if(heading<0.0) heading = 360.0  + heading;
        
        // Calculate the 3 point moving average of the magnitude of the 
        // acceleration vector
        mag = sqrt((ax*ax) + (ay*ay) + (az*az));
        avg = (buffer[0] + buffer[1] + mag) / 3;
        buffer[0] = buffer[1];
        buffer[1] = mag;
        // Count a step if the difference between the current and previous avg
        // point crosses a threshold
        if(sample_num > 1) {
            float dif1 = avg_buffer[1] - avg_buffer[0];
            float dif2 = avg_buffer[1] - avg;
            float peak_prominence = 0.01;
            if(dif1 > peak_prominence && dif2 > peak_prominence) {
                steps++;
            }
        }
        avg_buffer[0] = avg_buffer[1];
        avg_buffer[1] = avg;
        sample_num++;
        Thread::wait(200);
    }
}

void thread4(void const *args){
    while(1){
        float AO_value = AO;
        float DO_value = DO;
        //pc.printf("AO: %f \r\n", AO_value);
        //pc.printf("DO: %f \r\n", DO_value);
        if(AO < 0.7){
            int draw_temp = draw;
            int draw_c_temp = draw_c;
            draw = 0;
            draw_c = 0;
            mySpeaker.PlayNote(790.31,0.5,0.3);
            mySpeaker.PlayNote(939.85,0.5,0.3);
            lcd_mutex.lock();
            uLCD.cls();
            uLCD.color(RED);
            uLCD.text_height(2);
            uLCD.text_width(2);
            uLCD.set_font(FONT_7X8);
            uLCD.locate(1,2);
            uLCD.printf(" Rain");
            uLCD.locate(1,3);
            uLCD.printf("Warning!");
            Thread::wait(5000);
            uLCD.cls();
            lcd_mutex.unlock();
            draw = draw_temp;
            draw_c = draw_c_temp;
        }
        Thread::wait(3000);
    }
}

void thread5(void const *args){
    set_time(1256729737);  // Set RTC time to Wed, 28 Oct 2009 11:35:37
    while (1) {
        time_t seconds = time(NULL);
        char buffer[32];
        // Format changed to include seconds
        strftime(buffer, 32, "%I:%M:%S %p\n", localtime(&seconds));
        //pc.printf("Time as a custom formatted string = %s", buffer);
        if(ready){
            lcd_mutex.lock();
            uLCD.filled_rectangle(0, 0, 30, 5, 0x66ff66);
            lcd_mutex.unlock();
        }

        // printf text only full screen mode demo
        if(draw){
            if(ready){
                lcd_mutex.lock();
                uLCD.filled_rectangle(0, 0, 31, 15, GREEN);
                uLCD.color(WHITE);
                uLCD.text_height(2);
                uLCD.text_width(2);
                uLCD.set_font(FONT_7X8);
                uLCD.locate(0,2);
                uLCD.printf("%s", buffer);
                lcd_mutex.unlock();
            }else{
                lcd_mutex.lock();
                uLCD.color(WHITE);
                uLCD.text_height(2);
                uLCD.text_width(2);
                uLCD.set_font(FONT_7X8);
                uLCD.locate(1,3);
                uLCD.printf("Welcome");
                lcd_mutex.unlock();
            }
        }
        Thread::wait(1000);
    }
}

void thread6(void const *args){
    while(1){
        if(fan){
            mot.write(1.0f); // Set PWM duty cycle to 100%
        }else{
            mot.write(0.0f); // Turn off PWM (duty cycle 0%)
        }
    }
}

int main()
{
    uLCD.cls();
    uLCD.display_control(LANDSCAPE_R);
    Thread t1(thread1); //start thread1
    Thread t2(thread2); //start thread2
    Thread t3(thread3); //start thread3
    Thread t4(thread4); //start thread4
    Thread t5(thread5); //start thread5
    Thread t6(thread6); //start thread6

    mu.startUpdates();//start measuring the distance
    while(1)
    {
        //Do something else here
        mu.checkDistance();     //call checkDistance() as much as possible, as this is where
                                //the class checks if dist needs to be called.
        Thread::wait(100);
    }
}
~~~

## Future Plan

Moving forward, we are planning some upgrades to our project. We want to make things neater by using custom-designed printed circuit boards (PCBs) to get rid of wiring hassles entirely. Also, when it comes to the hat case, our goal is to use 3D printing to create a sleek enclosure. The idea is to hide all the electronic components inside the case, giving it a clean and polished look. These changes are aimed at making the project more user-friendly and improving its overall appearance and functionality. Furthermore, we want to refine the way we attach the uLCD and fan. Moving away from hot glue used in the prototype, we are opting for a more polished approach by 3D printing and laser-cutting attachment parts, to elevate the overall quality and feel of the product.
