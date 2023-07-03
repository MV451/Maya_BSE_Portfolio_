# Customized Biometrics Display

My project is a customized pulse oximeter.  It will have a SpO2, temperature, and heart rate sensor.  The device will also be able to plot the person’s pulse on a graph.  Switches will also be used to change between these modes.  

Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Maya V | UPA | Bioengineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone
For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Second Milestone
For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# First Milestone

In this first milestone I was able to connect my arduino to the MAX30101 and test out each sensor that is integrated in the board which came with libraries so I would not need to make the code from scratch.   After connecting the MAX30101 to the arduino I needed to figure out how to use a switch to change between the modes.  For this first milestone I focused on just switching between two modes: SpO2 and the pulse plotter.  After doing research on how to structure the code for a switch like this I was able to combine the code from both modes into one file and how the device is able to change between these modes.  

Getting to this point was challenging since I have not had any coding experience or worked with an arduino before.  I also spent a lot of time trying to connect an OLED monitor to display the data from the sensor instead of it just being displayed on the computer.  However, the display was not compatible with the codes I needed to use for the device.  To fix this a different monitor was ordered.  I will try to connect this new monitor for my second milestone.  I also need to add a second switch to the device so it can switch between all four modes instead of just the two. 

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Starter Project
Introduction:

My starter project was a mini cat lamp that lights up whenever it is in the dark.  The purpose of this starter project was mainly for me to gain experience in soldering multiple pieces together.  The parts of the cat body are made up of the same material circuit boards are made up of so it will not burn when soldering.  The project also came with a photoresistor, transistor, LED, 100k resistor, switch, and battery.

Materials:

- Cat lamp pieces
- Photoresistor: A type of light dependent resistor.  The more light shining on it means there will be less resistance.
- Transistor: Is like a switch that only allows current to move through it when there is current or voltage.
- LED: Stands for light emitting diode.  Current can only flow one way through (the longer leg is positive while the shorter leg is negative), so it is important to have it    oriented correctly in the circuit. 
- 100k resistor: Impedes the circuit’s current and prevents the LED from burning out.
- Switch: Opens or closes the circuit so the cat lamp has the ability to turn completely off regardless of the amount of light in the room.
- CR 2032 Coin Battery
- Coin Battery Holder

Process:

Soldering all of the cat pieces was fairly simple, however the paper instructions were slightly different than the instructional video that it came with (the cat was in a different orientation).  This inconsistency did not affect how the cat lamp functions though, just the appearance.  When looking closely at the body of the cat the circuit is able to be seen.  I had trouble understanding the circuit at the beginning since it seemed as if it was in series.  However, after researching some more I realized that the circuit had to be in parallel in order for the cat lamp to work.  The lines on the cat lamp marking the circuit pathway may have just been imprinted incorrectly.  After figuring this out, I was able to draw out the circuit to understand how the cat lamp functions.  The circuit in the cat lamp is wired to be in parallel which means the current has two pathways it can possibly flow through.  One path has the transistor and LED while the other has the photoresistor.  Current is actually the movement of electrons and electrons prefer to take the path of least resistance.  When light shines on  the photoresistor the resistance decreases making that pathway more favorable.  Since more electrons are going through the photoresistor pathway there is less current going through the pathway with the transistor and LED.  The reduced current is not enough to go past the transistor and light up the LED.  This is why the lamp does not light up when it is exposed to light.  However, when the lamp is in the dark the resistance of the photoresistor increases causing more current to go through the other pathway.  This current is strong enough to get past the transistor and light up the LED.  This is how the cat lamp is able to turn on whenever it is dark.  The cat lamp is also able to be turned on “manually” by covering the photoresistor. 

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

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
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
