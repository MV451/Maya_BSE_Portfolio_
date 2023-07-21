# Cardiac Monitor with Temperature Sensing Capabilities

My project is a student defined project that can record heart rate, temperature, plot the user’s pulse on a graph, and even has an EKG to measure the heart's electrical activity.  The user will be given instructions on an OLED display for how to use the device and the numerical data for their vitals.  This project was not easy to make and I ran into multiple obstacles.  However, in the end it was very rewarding to know that I was able to create and build my own project. 

<!--Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!-->

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Maya V | UPA | Bioengineering | Incoming Senior

<!--**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)

# Final Milestone

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>-->

# Third Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/rJv0AnRTgms" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Summary:
For this milestone I added the EKG (Electrocardiogram) to my project.  This proved to be extremely difficult since there were many things I needed to change in my code and wiring.  I needed to add an external power supply and another Arduino Nano.  Besides adding the EKG, I made changes such as removing the pull up resistors that I had for the A4 and A5 pins since they were unnecessary and may have slowed my device down.  

Components Used:

- x2 Arduino Nanos
- x16 Female to Male Jumper Wires
- x5 Male to Male Jumper Wires
- External Power Supply
- x2 1 foot Mini-B USB to USB A Cord
- Barrel Jack Adapter
- AD8232 Heart Monitor
- x60 Disposable Surface EKG Electrodes
- Electrode Cable (3 connecter)

How the Components Work Together

When I added the EKG I realized that there was too much noise interfering with the sensor and I needed to somehow reduce that.  The addition of an external power supply and another Arduino Nano works to reduce the electromagnetic fields around the EKG sensor so the data is readable.  The Arduinos are attached with a jumper wire on one of the digital pins.  This is how they are able to communicate with each other since the digital pins are able to send two types of signals (high and low) which work perfectly with the button.  When the button is pressed for the fourth time, the digital pin is set to high.  This is how the main Arduino tells the other Arduino to turn on the EKG.  Then when the button is pressed again, the digital pin reverts back to low which turns off the EKG. 

## Progress:
I made significant progress with this milestone since now my base project and the EKG are able to work together.  It took a long time to figure out how exactly to find the solution to what was causing the noise interfering with the EKG.  I needed to rewire my entire device and consolidate it onto two breadboards since I was originally using an extra breadboard for the button which was unnecessary.  Now he OLED monitor is able to display the instructions for how to use the cardiac monitor and the sensor mode it is on. 

## Challenges Faced
This milestone was difficult for me since the EKG was not like any of the other sensors I have in my device.  The EKG measures the electrical activity of the heart.  However, anything that is plugged into power creates an electromagnetic field.  This field interferes with the EKG causing the data to be noisy meaning that there are extra waves.  After doing some research and receiving help, I realized that I needed to separate the EKG from the rest of the devices since they were creating electromagnetic fields that interfered with the device.  This is why I ended up adding another Arduino Nano to my device and an external power supply.  I also found out that using a high-pass filter would lower the noise on my device.  This is a filter that blocks all of the low frequencies the sensor picks up while letting high frequencies “pass” onto the plotter.  I tried a low-pass filter originally, but that did not help as much as the high-pass filter.  All of these modifications significantly lowered the noise in the EKG plotter.

When I modified my device during this milestone something changed during the rewiring and in the code.  My device would not work at all after this which was alarming.  I needed to recheck all of the wiring and this is when I removed the two pull-up resistors since I wanted to remove anything that was not necessary (the pull-up resistors were initially meant for the OLED display that was not compatible with my device).  After I fixed my wiring and checked it over, I needed to fix the code.  I ended up needing to go back to an older version of my code that still worked.  I then modified it to include the EKG and the new instructions I added to the OLED display.  Although I needed to redo my entire project and go back to old code, I am proud that I was able to fix my project and include the EKG.

## Next Steps
The next part of my project for me will be to solder all of my part onto a perfboard since bread board connections are not the strongest.  I also would like to CAD a case for my device on Onshape to be 3D printed.  Something else I could add is modifying what is displayed on the OLED display such as making my own splash screen at the beginning when the device is initializing.  I will also write brief instructions to know when using the device such as how to properly close out the serial plotter.

# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/IoWeX2wKDNI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<!--For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>-->

## Summary:
For my second milestone, my goal was to alter my code so the cardiac monitor could switch between four modes and show the data on the OLED display.  The OLED display was supposed to display the vitals recorded from the MAX30101 sensor along with the pulse plotter graph.  This milestone was difficult since I needed to troubleshoot several problems and had to make a significant modification to my project to fix it.  I decided to remove the SpO2 sensor code since it was causing several complications such as preventing the OLED display from turning on and preventing my device from running since it took up too much memory.  I was hesitant to remove this, but doing so allowed me to complete the rest of my project.

Components Used:

- MAX30101 with Header Pins
- Small Rubber Band
- x9 Male to Male Jumper Wires
- x8 Female to Male Jumper Wires
- Small Push Button
- 128x64 OLED Display (SSD1306)
- 10K Ohm Resistor
- x2 470K Ohm Resistor
- Arduino Nano
- 1 foot Mini-B USB to USB A Cord
- Full Size Breadboard
- x2 Mini Breadboards

How the Components Work Together

The MAX30101 still functions in the same way as in the first milestone, however it now communicates with the button instead of the switch.  Since the buttons and switch have similar functions the wiring overall did not change much.  The main change to my device is the addition of the OLED display.  The OLED display uses I2C so it is connected to the Arduino nano on the A4 and A5 pins.  It also uses 5V.  I am still using three different breadboards for different parts of my device to keep the wiring organized.  One for the MAX30101, one for the button, and one for the Arduino.  I also color coded the wires so it is easy to identify which wire is connected to which pin.<--add the last two sentences to the first milestone?-->

## Progress:
Since I wanted to switch between more than two modes I needed to change my switch to a button.  For this I did research on how to code a button on Arduino.  I was able to alter this code to fit the three sensor modes and now am able to cycle between the sensors with it resetting to the first sensor after three presses.  This was difficult since I needed to include while loops in my code so the sensors would continue to run.  I altered the code so each sensor would set up only once, but also constantly check to see if the button was pressed again.  The OLED display was luckily not challenging to set up, especially since I had experience with my last OLED display.  The new OLED display is compatible with the SSD1306 (which is a type of driver), so most code works with it.  I did notice how the OLED address was 0x3C, so I needed to change that in the code since originally the address was 0x3D.  The OLED monitor was able to display all of the data except for the graph of the pulse plotter.  Since my device can now switch between modes and the OLED display is able to show the data, I am now done with the main part of my project and can start on my modifications!

## Challenges Faced
I faced multiple challenges during this milestone, especially with the SpO2 sensor.  The SpO2 sensor was accurate and took a while to set up, making cycling between modes take a long time.  It also took up a lot of memory in global variables on my Arduino and sometimes prevented it from running.  When I figured out that the SpO2 sensor was stopping the OLED display from even turning on I decided to remove it.  My main interest is in cardiac monitoring so although the SpO2 sensor was one of the main sensors on my device, I removed it in order to continue my project.

## Next Steps
I am excited to have finished the main part of my project and am now ready to start my third milestone.  In this milestone I will add the EKG (Electrocardiogram) sensor which requires a different board.  The OLED display also currently has space for more text on its screen so I am planning on adding instructions for how to use the device and the normal parameters the vital signs should be for each sensor.

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/nh_UaqvMNVQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Summary:
In this first milestone I was able to connect my arduino to the MAX30101.  I tested out each sensor that was integrated in the board.  The MAX30101 came with libraries so I did not need to make the code from scratch.  After connecting the MAX30101 to the Arduino, I needed to figure out how to use a switch to change between the modes.  For this first milestone, I focused on switching between two modes: SpO2 and the pulse plotter.  After doing research on how to structure the code for a switch, I was able to combine the code from both modes into one file so the device could cycle between these modes.  Now the MAX30101 board and the switch are connected to the Arduino and the switch can control which sensor is turned on.

Components Used:

- MAX30101 with Header Pins - Has the four sensor modes (pulse plotter, heart rate, SpO2, and temperature)
- Small Rubber Band - To put around MAX30101 board to stabilize finger
- x9 Male to Male Jumper Wires - To connect components
- x4 Female to Male Jumper Wires - To connect components
- Switch - To change between the two modes
- 10K Ohm Resistor - A pull-down resistor for the switch
- x2 470K Ohm Resistor - Used as pull-up resistors for MAX30101
- Arduino Nano - The microcontroller to upload code to
- 1 foot Mini-B USB to USB A Cord - Connects Arduino to computer
- Full Size Breadboard - All components are connected on this
- x2 Mini Breadboards - Used to hold up the OLED display

How the Components Work Together

The MAX30101 is a board that has the sensors that can record four different vital signs (heart rate, pulse, SpO2, and temperature).  The user is supposed to place their finger on the sensor where the light is flashing and use the mini rubberband to hold their finger in place since constant pressure achieves the best results.  NExt, female to male jumper wires were used to help connect the MAX30101 to the Arduino Nano.  Two 470K Ohm resistors were used as pullup resistors for the MAX30101 to stabilize the connection.  Another breadboard was used to have the circuit with the switch since there was not much room on the main breadboard.  This switch also needed a pulldown resistor.  The switch circuit and the MAX30101 all connect to the Arduino Nano while the Mini-B USB to USB A cord is was used to connect the device to my computer.

<!-- include link to website with the schematic for how to wire a button/switch on arduino-->

## Progress
I was able to learn how to connect the Arduino Nano to the MAX30101.  In order to do this, I needed to solder on some header pins so jumper wires could connect the board to the Arduino.  After I matched each pin to the pin on the Arduino Nano, I was able to test out each of the four sensors that was included in the MAX30101.  In order to turn each sensor on, I used the libraries that came with the MAX30101 and all of them were able to work (although the SpO2 sensor is not as accurate as it could be).  After I got that to work I wanted to connect a switch to the device so I could switch between modes.  Even though there are four different modes, I started off with just two so I could start off using a simpleswitch.  I found a schematic that showed how to connect a switch to an Arduino and how to structure the code.  Then I needed to find a way to add the code from the two sensors (SpO2 and pulse plotter) and integrate it into the code controlling the switch.  This was difficult since there were many things that needed to be defined and I needed to understand the code in order to know where they should be placed.  In the end I was able to combine all of the codes together and my device can now switch between recording SpO2 and the pulse plotter data.

## Challenges
Getting to this point was challenging since I have not had any coding experience or worked with an Arduino before.  It was difficult to combine the different codes for the SpO2 sensor and the pulse plotter into the code for the switch.  I also spent a lot of time trying to connect an OLED monitor to display the data from the sensor instead of it just being displayed on the computer.  However, the display was not compatible with the codes I needed to use for the device.  To fix this, a different monitor was ordered, but I was not able to receive it in time to include it in my first milestone.  I also struggled with learning how to use Arduino in general since I was unfamiliar with microcontrollers and C++.  

## Next Steps
Since I was unable to connect a monitor to my device for my first milestone I will try to connect the new monitor for my second milestone.  Hopefully the monitor will be able to change the data it displays when the switch is flipped.  It should also be able to display the pulse Plotter.  I need to add a second switch to the device so it can switch between all four modes instead of just the two.  This will require for me to learn more about how to code a switch.  I will need to figure out how to wire a second switch to my breadboard since it is running out of room.

<!--**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->

# Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/koEIfZc_ih4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Summary:
My starter project was a mini cat lamp that lights up whenever it is in the dark.  The purpose of this starter project was mainly for me to gain experience soldering multiple pieces together.  The parts of the cat body are made up of the same material as circuit boards so it would not burn when soldering.  The project also came with a photoresistor, transistor, LED, 100k resistor, switch, and battery.

Components Used:

- Cat lamp pieces
- Photoresistor: A type of light dependent resistor.  The more light shining on it means there will be less resistance.
- Transistor: Is like a switch that only allows current to move through it when there is current or voltage.
- LED: Stands for light emitting diode.  Current can only flow one way through (the longer leg is positive while the shorter leg is negative), so it is important to have it    oriented correctly in the circuit. 
- 100k resistor: Impedes the circuit’s current and prevents the LED from burning out.
- Switch: Opens or closes the circuit so the cat lamp has the ability to turn completely off regardless of the amount of light in the room.
- CR 2032 Coin Battery
- Coin Battery Holder

How the Parts Work Together:
The cat lamp came with pieces that were similar to the material a circuit board is made up of and is what makes up most of the lamp.  Soldering all of the parts to the cat lamp not only attaches all of the pieces together, but also connected the other components to the circuit such as the transistor and LED. The circuit in the cat lamp is wired to be in parallel which means the current has two pathways to flow through.  One path has the transistor and LED while the other has the photoresistor.  Current is the movement of electrons and electrons prefer to take the path of least resistance.  When light shines on the photoresistor, the resistance decreases making that pathway more favorable.  With more electrons are going through the photoresistor pathway, less current goes through the pathway with the transistor and LED.  The reduced current is not enough to go past the transistor and light up the LED.  This is why the lamp does not light up when it is exposed to light.  However, when the lamp is in the dark, the resistance of the photoresistor increases making the pathway less favorable and causing more current to go through the other pathway.  This current is strong enough to get past the transistor and light up the LED.  This is how the cat lamp is able to turn on whenever it is dark.

## Progress:
I was able to solder all of the pieces of the cat lamp together and understand exactly how it works.  All of the pieces of the cat lamp body were soldered together except for the arms which are removable.  The cat lamp can now be switched on and off and turns on when it is in the dark.  This project was simple and did not take long for me to complete overall.

## Challenges:
Soldering all of the cat pieces was fairly simple, however the paper instructions was slightly different than the instructional video  it came with (the cat was in a different orientation).  This inconsistency did not affect how the cat lamp functions though, just the appearance.  When looking closely at the body of the cat, the circuit is able to be seen.  I had trouble understanding the circuit at the beginning since it seemed as if it was in series.  However, after researching some more, I realized that the circuit had to be in parallel in order for the cat lamp to work.  The lines on the cat lamp marking the circuit pathway may have just been imprinted incorrectly.  After figuring this out, I was able to draw out the circuit to understand exactly how the cat lamp functions.  

## Next Steps:
Aftr finished the cat lamp I now have experience soldering and reviewed how circuits work.  My next step is to start on my intensive project.  I will need to solder a little, but this project will mainly involve an Arduino and learning how to compile all of the code together for the sensor.  I also will learn how to connect the sensor to the Arduino with jumper wires.

<!--**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>-->

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
<!---Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```-->
## Main Code
<pre style="background:#fdfdfd : border:none; height:40pc">
/* This is my main code that is supposed to be uploaded to the main Arduino (attached to the OLED display and the MAX30101).  The EKG code is supposed to be opened up in a separate window and uploaded to the second Arduino. */

//Fxns need to be declared at the beginning of the code so the computer knows it's coming (I put all of the actual fxns at the end)
void Pulse();
void Temp();
void Bpm();

// this constant won't change:
const int buttonPin = 2;  // the pin that the pushbutton is attached to

// Variables will change:
int buttonMode = 0;       // counter for the number of button presses
int buttonState = 0;      // current state of the button
int lastButtonState = 0;  // previous state of the button

/***************From Old Four Mode Code***************/

byte ledBrightness = 60;  //Options: 0=Off to 255=50mA
byte sampleAverage = 4;   //Options: 1, 2, 4, 8, 16, 32
byte ledMode = 2;         //Options: 1 = Red only, 2 = Red + IR, 3 = Red + IR + Green
byte sampleRate = 100;    //Options: 50, 100, 200, 400, 800, 1000, 1600, 3200
int pulseWidth = 411;     //Options: 69, 118, 215, 411
int adcRange = 4096;      //Options: 2048, 4096, 8192, 16384

/***************Generally needed for the sensors?***************/
#include <Wire.h>
#include "MAX30105.h"
MAX30105 particleSensor;
// #define MAX_BRIGHTNESS 255

/***************Generally needed for the sensors?***************/
#include "heartRate.h"

const byte RATE_SIZE = 4;  //Increase this for more averaging. 4 is good.
byte rates[RATE_SIZE];     //Array of heart rates
byte rateSpot = 0;
long lastBeat = 0;  //Time at which the last beat occurred

float beatsPerMinute;
int beatAvg;

/********From OLED********/

#include <SPI.h>
#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>

#define SCREEN_WIDTH 128  // OLED display width, in pixels
#define SCREEN_HEIGHT 64  // OLED display height, in pixels

// Declaration for an SSD1306 display connected to I2C (SDA, SCL pins)
// The pins for I2C are defined by the Wire-library.
// On an arduino UNO:       A4(SDA), A5(SCL)
// On an arduino MEGA 2560: 20(SDA), 21(SCL)
// On an arduino LEONARDO:   2(SDA),  3(SCL), ...
#define OLED_RESET -1        // Reset pin # (or -1 if sharing Arduino reset pin)
#define SCREEN_ADDRESS 0x3C  ///< See datasheet for Address; 0x3D for 128x64, 0x3C for 128x32
Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, OLED_RESET);

// #define NUMFLAKES     10 // Number of snowflakes in the animation example

#define LOGO_HEIGHT 16
#define LOGO_WIDTH 16
static const unsigned char PROGMEM logo_bmp[] = {
  0b00000000, 0b11000000,
  0b00000001, 0b11000000,
  0b00000001, 0b11000000,
  0b00000011, 0b11100000,
  0b11110011, 0b11100000,
  0b11111110, 0b11111000,
  0b01111110, 0b11111111,
  0b00110011, 0b10011111,
  0b00011111, 0b11111100,
  0b00001101, 0b01110000,
  0b00011011, 0b10100000,
  0b00111111, 0b11100000,
  0b00111111, 0b11110000,
  0b01111100, 0b11110000,
  0b01110000, 0b01110000,
  0b00000000, 0b00110000
};


void setup() {
  // initialize the button pin as a input:
  pinMode(buttonPin, INPUT);
  pinMode(11, OUTPUT);
  digitalWrite(11, LOW);
  // initialize serial communication:
  //Serial.begin(115200);

  /***************From SpO2 Setup***************/

  // Serial.begin(115200);  // initialize serial communication at 115200 bits per second:

  // pinMode(pulseLED, OUTPUT);
  // pinMode(readLED, OUTPUT);

  //Maybe I can remove the code above????
  /********From OLED********/

  // SSD1306_SWITCHCAPVCC = generate display voltage from 3.3V internally
  if (!display.begin(SSD1306_SWITCHCAPVCC, SCREEN_ADDRESS)) {
    //Serial.println(F("SSD1306 allocation failed"));
    for (;;)
      ;  // Don't proceed, loop forever
  }

  display.clearDisplay();
  /*display.setTextSize(1);  // Draw 2X-scale text
  display.setTextColor(SSD1306_WHITE);
  display.println(F("Initializing..."));
  display.println();*/
  display.setTextSize(2);  // Draw 2X-scale text
  display.setTextColor(SSD1306_WHITE);
  // display.setCursor(0, 0);
  display.println(F("Open"));
  display.println(F("Plotter"));
  display.setTextSize(1);  // Draw 2X-scale text
  display.println(F("initializing..."));
  display.println();
  display.println(F("Note: Opening plotter"));
  display.println(F("resets device"));
  display.println();

  display.display();  // Show initial text
  delay(3000);

  // Show initial display buffer contents on the screen --
  // the library initializes this with an Adafruit splash screen.
  display.display();
  delay(500);  // Pause for 0.5 seconds

  // Clear the buffer
  // display.clearDisplay();

  // Show the display buffer on the screen. You MUST call display() after
  // drawing commands to make them visible on screen!
  display.display();
  delay(20);


  // Initialize sensor
  if (!particleSensor.begin(Wire, I2C_SPEED_FAST))  //Use default I2C port, 400kHz speed
  {
    Serial.println(F("MAX30105 was not found. Please check wiring/power."));
    while (1)
      ;
  }
  /********From OLED********/

  // // SSD1306_SWITCHCAPVCC = generate display voltage from 3.3V internally
  // if (!display.begin(SSD1306_SWITCHCAPVCC, SCREEN_ADDRESS)) {
  //   //Serial.println(F("SSD1306 allocation failed"));
  //   for (;;)
  //     ;  // Don't proceed, loop forever
  // }

  // Show initial display buffer contents on the screen --
  // the library initializes this with an Adafruit splash screen.
  // display.display();
  // delay(2000);  // Pause for 2 seconds

  // Clear the buffer
  // display.clearDisplay();

  // Show the display buffer on the screen. You MUST call display() after
  // drawing commands to make them visible on screen!
  // display.display();
  // delay(2000);
}

void loop() {

  if (buttonMode == 0) {
    Pulse();
    delay(500);
  } else if (buttonMode == 1) {
    Bpm();
    delay(500);
  } else if (buttonMode == 2) {
    Temp();
    delay(500);
  } else if (buttonMode == 3) {
    EKG();
    delay(500);
  } else {
    buttonMode = -1;
  }
}

/*************************Bpm*************************/

void Bpm() {

  /*// Initialize sensor
  if (!particleSensor.begin(Wire, I2C_SPEED_FAST))  //Use default I2C port, 400kHz speed
  {
    //Serial.println("MAX30105 was not found. Please check wiring/power. ");
    while (1)
      ;
  }*/
  /********OLED intro*********/
  display.clearDisplay();
  display.setTextSize(2);  // Draw 2X-scale text
  display.setTextColor(SSD1306_WHITE);
  display.setCursor(0, 0);
  display.println(F("Heart Rate"));
  display.println(F("Sensor"));
  //  display.println(F("Sensor"));
  display.display();  // Show initial text
  delay(20);

  particleSensor.setup();                     //Configure sensor with default settings
  particleSensor.setPulseAmplitudeRed(0x0A);  //Turn Red LED to low to indicate sensor is running
  particleSensor.setPulseAmplitudeGreen(0);   //Turn off Green LED

  while (1) {
    long irValue = particleSensor.getIR();

    if (checkForBeat(irValue) == true) {
      //We sensed a beat!
      long delta = millis() - lastBeat;
      lastBeat = millis();

      beatsPerMinute = 60 / (delta / 1000.0);

      if (beatsPerMinute < 255 && beatsPerMinute > 20) {
        rates[rateSpot++] = (byte)beatsPerMinute;  //Store this reading in the array
        rateSpot %= RATE_SIZE;                     //Wrap variable

        //Take average of readings
        beatAvg = 0;
        for (byte x = 0; x < RATE_SIZE; x++)
          beatAvg += rates[x];
        beatAvg /= RATE_SIZE;
      }

      /********added from OLED display********/

      display.clearDisplay();

      display.setTextSize(2);  // Draw 2X-scale text
      display.setTextColor(SSD1306_WHITE);
      display.setCursor(0, 0);
      display.print(F("HR= "));
      display.print(beatAvg);
      display.println(F(" bpm"));

      display.setTextSize(1);  // Draw 2X-scale text
      display.setTextColor(SSD1306_WHITE);
      display.println();
      display.println("Avg bpm = 60-100 bpm");

      display.display();  // Show initial text
      delay(20);



      display.display();  // Show initial text
      delay(20);
    }
    /********for button********/
    // Serial.println(particleSensor.getIR());  //Send raw data to plotter

    buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH) {
      buttonMode = 2;
      return;
    }
  }
}
/*************************Pulse Plotter*************************/

void Pulse() {
  Serial.begin(115200);
  //Setup to sense a nice looking saw tooth on the plotter
  byte ledBrightness = 0x1F;  //Options: 0=Off to 255=50mA
  byte sampleAverage = 8;     //Options: 1, 2, 4, 8, 16, 32
  byte ledMode = 3;           //Options: 1 = Red only, 2 = Red + IR, 3 = Red + IR + Green
  int sampleRate = 100;       //Options: 50, 100, 200, 400, 800, 1000, 1600, 3200
  int pulseWidth = 411;       //Options: 69, 118, 215, 411
  int adcRange = 4096;        //Options: 2048, 4096, 8192, 16384

  particleSensor.setup(ledBrightness, sampleAverage, ledMode, sampleRate, pulseWidth, adcRange);  //Configure sensor with these settings

  //Arduino plotter auto-scales annoyingly. To get around this, pre-populate
  //the plotter with 500 of an average reading from the sensor

  //Take an average of IR readings at power up
  const byte avgAmount = 64;
  long baseValue = 0;
  for (byte x = 0; x < avgAmount; x++) {
    baseValue += particleSensor.getIR();  //Read the IR value
  }
  baseValue /= avgAmount;

  //Pre-populate the plotter so that the Y scale is close to IR values
  for (int x = 0; x < 500; x++)
    Serial.println(baseValue);

  /********OLED intro*********/
  display.clearDisplay();
  display.setTextSize(2);  // Draw 2X-scale text
  display.setTextColor(SSD1306_WHITE);
  display.setCursor(0, 0);
  display.println(F("Pulse"));
  display.println(F("Plotter"));

  display.display();  // Show initial text
  delay(1000);

  while (1) {
    Serial.println(particleSensor.getIR());  //Send raw data to plotter

    /********OLED display********/
    display.clearDisplay();

    display.setTextSize(1);  // Draw 2X-scale text
    display.setTextColor(SSD1306_WHITE);
    display.setCursor(0, 0);
    display.println("View pulse plotter on");
    display.println("computer");
    display.println();
    display.println("Stop & close plotter");
    display.println("when finished");
    display.display();  // Show initial text
    delay(20);

    /*********Button*********/
    buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH) {
      Serial.end();
      buttonMode = 1;
      return;
    }
  }
}

/*************************Temperature*************************/

void Temp() {

  //The LEDs are very low power and won't affect the temp reading much but
  //you may want to turn off the LEDs to avoid any local heating
  particleSensor.setup(0);  //Configure sensor. Turn off LEDs
  //particleSensor.setup(); //Configure sensor. Use 25mA for LED drive

  particleSensor.enableDIETEMPRDY();  //Enable the temp ready interrupt. This is required.


  /********OLED intro*********/
  display.clearDisplay();
  display.setTextSize(2);  // Draw 2X-scale text
  display.setTextColor(SSD1306_WHITE);
  display.setCursor(0, 0);
  display.println(F("Temp"));
  display.println(F("Sensor"));

  display.display();  // Show initial text
  delay(1000);

  /****in loop****/
  while (1) {
    // float temperature = particleSensor.readTemperature();

    // Serial.print("temperatureC=");
    // Serial.print(temperature, 4);

    float temperatureF = particleSensor.readTemperatureF();
    float temperature = particleSensor.readTemperature();

    // Serial.print(" temperatureF=");
    // Serial.print(temperatureF, 4);

    // Serial.println();

    /********added from OLED display********/

    display.clearDisplay();

    display.setTextSize(2);  // Draw 2X-scale text
    display.setTextColor(SSD1306_WHITE);
    display.setCursor(0, 0);
    display.println(F("Temp in F="));
    display.println(temperatureF);
    display.setTextSize(1);  // Draw 1X-scale text
    display.setTextColor(SSD1306_WHITE);
    display.println();
    display.print(F("Temp in C = "));
    display.println(temperature);
    display.println();
    display.print(F("Avg Temp = ~84F/~29C"));
    display.display();  // Show initial text
    delay(20);

    /********Button********/

    buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH) {
      buttonMode = 3;
      return;
    }
  }
}

/*************************EKG*************************/

void EKG() {

  digitalWrite(11, HIGH);

  /********OLED intro*********/
  display.clearDisplay();
  display.setTextSize(2);  // Draw 2X-scale text
  display.setTextColor(SSD1306_WHITE);
  display.setCursor(0, 0);
  display.println(F("EKG"));
  display.setTextSize(1);
  display.setTextColor(SSD1306_WHITE);
  display.println();
   display.println(F("Switch to EKG window"));
  //  display.println();
  // display.println(F("Attach 3 electrodes"));

  display.display();  // Show initial text
  delay(3000);
  display.clearDisplay();
  delay(10);

  while (1) {

    /********OLED********/
    display.setTextSize(1);
    display.setCursor(0, 0);
    display.setTextColor(SSD1306_WHITE);
    display.println(F("Close plotter when"));
    display.println(F("done"));
    display.println();
    display.println(F("Less movement reduces"));
    display.println(F("noise interference"));
     display.println();
    display.println(F("Will take a moment to"));
    display.println(F("switch back to pulse"));

      display.display();  // Show initial text
    delay(20);

    /********Button********/

    buttonState = digitalRead(buttonPin);
    if (buttonState == HIGH) {
      buttonMode = 0;
      digitalWrite(11, LOW);

      return;
    }
  }
}
</pre>

## EKG Code
<pre style="background:#fdfdfd : border:none; height:40pc">
  
/* 
This code is for the EKG and should be uploaded to the second Arduino.  
Note: This code works the best when everything is directly connected to the Arduino or everything is connected with a perfboard. It is also better if I hold my breath to limit
motion artifacts (extraneous noise that interferes with the EKG reading).

I got the code from this website: 
https://circuitdigest.com/microcontroller-projects/understanding-ecg-sensor-and-program-ad8232-ecg-sensor-with-arduino-to-diagnose-various-medical-conditions

 * VARIABLES

 * count: variable to hold count of rr peaks detected in 10 seconds

 * flag: variable that prevents multiple rr peak detections in a single heatbeat

 * hr: HeartRate (initialised to 72)

 * hrv: Heart Rate variability (takes 10-15 seconds to stabilise)

 * instance1: instance when heart beat first time

 * interval: interval between second beat and first beat

 * timer: variable to hold the time after which hr is calculated

 * value: raw sensor value of output pin

 */

 int val; 

long instance1 = 0, timer;

double hrv = 0, hr = 72, interval = 0;

int value = 0, count = 0;

bool flag = 0;

#define shutdown_pin 10

#define threshold 100  // to identify R peak

#define timer_value 10000  // 10 seconds timer to calculate hr

/********High-pass********/

template<int order>  // order is 1 or 2
class HighPass {
private:
  float a[order];
  float b[order + 1];
  float omega0;
  float dt;
  bool adapt;
  float tn1 = 0;
  float x[order + 1];  // Raw values
  float y[order + 1];  // Filtered values

public:
  HighPass(float f0, float fs, bool adaptive) {
    // f0: cutoff frequency (Hz)
    // fs: sample frequency (Hz)
    // adaptive: boolean flag, if set to 1, the code will automatically set
    // the sample frequency based on the time history.

    omega0 = 6.28318530718 * f0;
    dt = 1.0 / fs;
    adapt = adaptive;
    tn1 = -dt;
    for (int k = 0; k < order + 1; k++) {
      x[k] = 0;
      y[k] = 0;
    }
    setCoef();
  }

  void setCoef() {
    if (adapt) {
      float t = micros() / 1.0e6;
      dt = t - tn1;
      tn1 = t;
    }

    float alpha = omega0 * dt;
    if (order == 1) {
      float alphaFactor = 1 / (1 + alpha / 2.0);
      a[0] = -(alpha / 2.0 - 1) * alphaFactor;
      b[0] = alphaFactor;
      b[1] = -alphaFactor;
    }
    if (order == 2) {
      float alpha = omega0 * dt;
      float dtSq = dt * dt;
      float c[] = { omega0 * omega0, sqrt(2) * omega0, 1 };
      float D = c[0] * dtSq + 2 * c[1] * dt + 4 * c[2];
      b[0] = 4.0 / D;
      b[1] = -8.0 / D;
      b[2] = 4.0 / D;
      a[0] = -(2 * c[0] * dtSq - 8 * c[2]) / D;
      a[1] = -(c[0] * dtSq - 2 * c[1] * dt + 4 * c[2]) / D;
    }
  }

  float filt(float xn) {
    // Provide me with the current raw value: x
    // I will give you the current filtered value: y
    if (adapt) {
      setCoef();  // Update coefficients if necessary
    }
    y[0] = 0;
    x[0] = xn;
    // Compute the filtered values
    for (int k = 0; k < order; k++) {
      y[0] += a[k] * y[k + 1] + b[k] * x[k];
    }
    y[0] += b[order] * x[order];

    // Save the historical values
    for (int k = order; k > 0; k--) {
      y[k] = y[k - 1];
      x[k] = x[k - 1];
    }

    // Return the filtered value
    return y[0];
  }
};

// Filter instance
HighPass<2> lp(20, 1e3, true);


void setup() {

  Serial.begin(115200);

  pinMode(8, INPUT);  // Setup for leads off detection LO +

  pinMode(9, INPUT);  // Setup for leads off detection LO -

  pinMode(11, INPUT);  // Digital read the mode

  Serial.println("Min:0,Max:1023");  //***********************I dont know if I actually need this or if it's messing up my code
}

void loop() {

  val = digitalRead(11);

  if (val == 1) {

    if ((digitalRead(8) == 1) || (digitalRead(9) == 1)) {

      Serial.println("leads off!");

      digitalWrite(shutdown_pin, LOW);  //standby mode

      instance1 = micros();

      timer = millis();

    }

    else {

      digitalWrite(shutdown_pin, HIGH);  //normal mode

      value = analogRead(A0);

      value = map(value, 250, 400, 0, 100);  //to flatten the ecg values a bit

      if ((value > threshold) && (!flag)) {

        count++;

        Serial.println("in");

        flag = 1;

        interval = micros() - instance1;  //RR interval

        instance1 = micros();

      }

      else if ((value < threshold)) {

        flag = 0;
      }

      if ((millis() - timer) > 10000) {
        // used to be *6
        hr = count * 10;

        timer = millis();

        count = 0;
      }
      // this used to be divided by 60
      hrv = hr / 30 - interval / 1000000;

      /********High-pass********/
      // Read pin A0 and compute current in mA
      // -- replace these two lines with your sensor readings --
      float t = millis() / 1000.0;
      float xn = sin(2 * PI * 2 * t) + 0.5 * cos(2 * PI * 50 * t);

      // Compute the filtered signal
      float yn = lp.filt(value);

      Serial.print(hr);

      Serial.print(",");

      Serial.print(hrv);

      Serial.print(",");

      Serial.println(yn);

      delay(15);
    }
  }
  delay(10);
}
  
</pre>

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Nano | The microcontroller for this device and where the code is uploaded to | $26.50 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|
| MAX30101 | Board with the four sensing capabilites.  I used three (pulse plotter, heart rate, temperature sensor) since the SpO2 sensor did not work well. | $22.50 | <a href="https://www.sparkfun.com/products/16474"> Link </a> |
|:--:|:--:|:--:|:--:|
| Single Lead Heart Rate Monitor - AD8232 | EKG Sensor | $21.50 | <a href="https://www.sparkfun.com/products/12650"> Link </a> |
|:--:|:--:|:--:|:--:|
| Sensor Cable - Electrode Pads (3 connector) | Connects with AD8232 and the three electrodes on the user's chest| $5.50 | <a href="https://www.sparkfun.com/products/12970"> Link </a> |
|:--:|:--:|:--:|:--:|
| OLED Display | Used to show numerical vital signs | $14.99 | <a href="https://www.amazon.com/Hosyond-Display-Self-Luminous-Compatible-Raspberry/dp/B09C5K91H7?keywords=0.96%2Binch%2Boled&qid=1670424637&sprefix=0.96%2Caps%2C100&sr=8-1-spons&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExVE9XUUM4UDQ1OFROJmVuY3J5cHRlZElkPUExMDExOTk0MTBDMzBDR0VNTlRPMSZlbmNyeXB0ZWRBZElkPUEwMjI3NTk2M0xBSTNXUVdWTVFMMyZ3aWRnZXROYW1lPXNwX2F0ZiZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU%3D&linkCode=sl1&tag=howtoelect0e4-20&linkId=6fe68cb2d4629728f64de60fcb2d9ca0&language=en_US&ref_=as_li_ss_tl&th=1"> Link </a> |
|:--:|:--:|:--:|:--:|
| Power Supply Module | EKG sensor gets power from this supply to reduce noise | $8.99 | <a href="https://www.amazon.com/HiLetgo-Supply-Module-Prototype-Breadboard/dp/B00HJ6AE72/ref=pd_lpo_sccl_1/141-3397973-3298860?pd_rd_w=61m0Z&content-id=amzn1.sym.116f529c-aa4d-4763-b2b6-4d614ec7dc00&pf_rd_p=116f529c-aa4d-4763-b2b6-4d614ec7dc00&pf_rd_r=T9CGYP5BSFZSX63VA3HB&pd_rd_wg=1kDND&pd_rd_r=f8b85e16-8bec-4fc5-8ff6-a7b427b19fd7&pd_rd_i=B00HJ6AE72&psc=1"> Link </a> |
|:--:|:--:|:--:|:--:|
| AC to Barrel Connector | Plugs Power Module into outlet | $6.50 | <a href="https://www.sparkfun.com/products/15312"> Link </a> |
|:--:|:--:|:--:|:--:|
| 30cm 3.0 USB to Mini USB cable| Connects Arduino Nano to Computerfor uploading code and power| $10.13 | <a href="https://www.amazon.com/30cm-Cable-arduino-Nano-Mini/dp/B09PBJJBVJ"> Link </a> |
|:--:|:--:|:--:|:--:|
| Black Pushbutton | The button used to switch between modes | $0.55 | <a href="https://www.sparkfun.com/products/9190"> Link </a> |
|:--:|:--:|:--:|:--:|
| Jumper Wires | Connects all components together | $2.10 | <a href="[https://www.sparkfun.com/products/9190](https://www.sparkfun.com/products/12796)"> Link </a> |
|:--:|:--:|:--:|:--:|
| 10K Ohm Resistor | Used as a pull-down resistor for pushbutton | $1.25 | <a href="https://www.sparkfun.com/products/14491"> Link </a> |
|:--:|:--:|:--:|:--:|
| 3m Red Dot Monitoring Electrodes | Electrodes used for the EKG and placed on the user's chest - connects to the sensor cable with electrode pads | $10.32 | <a href="https://www.amazon.com/3m-Red-Dot-Monitoring-Electrode/dp/B0015TI4G2"> Link </a> |


# Other Resources/Links
Here are some other websites and resources that helped me make my project.
- [Pushbutton/Switch Code](https://docs.arduino.cc/built-in-examples/digital/Button)
- [Website with EKG Code](https://circuitdigest.com/microcontroller-projects/understanding-ecg-sensor-and-program-ad8232-ecg-sensor-with-arduino-to-diagnose-various-medical-conditions)
- [MAX30101 Hookup Guide](https://learn.sparkfun.com/tutorials/sparkfun-photodetector-max30101-hookup-guide)
- [AD8232 Heart Rate Monitor Hookup Guide](https://learn.sparkfun.com/tutorials/ad8232-heart-rate-monitor-hookup-guide?_gl=1*1cra7qz*_ga*MjExOTM1OTQxMC4xNjg5MDE2OTcz*_ga_T369JS7J9N*MTY4OTAxNjk3My4xLjAuMTY4OTAxNjk3My4wLjAuMA..)
- [High-Pass Filter Code for EKG](https://github.com/curiores/ArduinoTutorials/blob/main/BasicFilters/ArduinoImplementations/HighPass/HighPass.ino)


