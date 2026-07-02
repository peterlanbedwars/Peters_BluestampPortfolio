# Knee Rehabilitation Device
Ever been hurt your knee in your respective sport? look no further than this knee rehabilitation device. This device brings comfort to your injury and helps you recover faster. Heres how you can make your own!
You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Peter L | Basis Independent Silicon Valley | Mechanical Engineering | Incoming Sophmor

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/CaCazFBhYKs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

The flex sensor connects to pin A6 on the Arduino and works by changing its electrical resistance when it bends. The code reads this as a number between 0 and 1023 using analogRead(), which represents how much voltage is coming through the sensor at that moment. Since that raw number doesn't mean anything by itself, the code uses map() to convert it into a real angle, from 0 to 130 degrees, based on two reference points: what the sensor reads when totally flat, and what it reads when bent all the way. Those two reference numbers had to be found by testing the sensor and writing down what it actually showed on the screen, since every sensor reads slightly differently. One extra line, constrain(), makes sure the angle never goes above 130 or below 0, even if the sensor gives a slightly weird reading.
The buzzer is connected to pin 3 and uses a function called tone() instead of just turning it on and off, because a piezo buzzer needs a vibrating signal to actually make sound, not just a steady flow of power. In the code, there's a constant called triggerAngle set to 85 degrees, and every time the program runs, it checks if the current knee angle is at or above that number. If it is, the buzzer turns on; if not, it stays off. This check happens constantly, over and over, so the buzzer can react instantly as soon as the angle crosses that 85-degree mark, even while other parts of the code are running.
The gyroscope and accelerometer are both built into one sensor board, and the code talks to them using a connection called I2C, which only needs two wires (SDA and SCL) even though there are two separate sensor chips. The gyroscope measures how fast something is spinning, and the code converts its raw numbers into degrees per second so they're easier to understand. The accelerometer measures movement in three directions at once (X, Y, and Z), and the code combines all three into one single number using some math (basically the Pythagorean theorem in 3D). Since gravity is always pulling down even when nothing is moving, the code also subtracts that constant gravity number out, so what's left over actually represents real movement instead of just gravity sitting there.
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
| Arduinio Nano Esp32 | The micro controller that connects gyroscope, accelarometer, and flex sensor | $14.64 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://store-usa.arduino.cc/products/nano-esp32)"> Link </a> |
| Adafruit LSM6DS3TR-C+LIS3MDL Accelerometer | tracks the angular velocity along with the acceration from the x,y, and z axis | $3.33 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.adafruit.com/product/5543?gad_source=1&gclid=Cj0KCQjwhb60BhClARIsABGGtw8-jY7wSMWS0FXfzOjqk8mHnPteYpW1C7iLXs6zfJK6qxsxANZ_MVoaAqhWEALw_wcB)"> Link </a> |
| Flex Sensor(4.5”) | measures the degree of the angle the knee is bending| $17.95 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |


# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
