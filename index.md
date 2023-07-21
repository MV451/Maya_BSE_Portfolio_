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

- MAX30101 with Header Pins
- Small Rubber Band
- x9 Male to Male Jumper Wires
- x4 Female to Male Jumper Wires
- Switch
- 10K Ohm Resistor
- x2 470K Ohm Resistor
- Arduino Nano
- 1 foot Mini-B USB to USB A Cord
- Full Size Breadboard
- x2 Mini Breadboards

How the Components Work Together

<!-- check to see why the pullup resistor was used-->
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
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

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

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here. -->
