# How to Play

Circles fall from the top of the screen at random horizontal positions.
Use the two buttons to move the paddle left and right to catch them.
You have 30 seconds so, catch as many circles as you can before time runs out.
Your score is shown on screen at the end of the round.

# Hardware: (Qty included)
- ESP32 Dev Module	1
- 1.3" OLED screen	1
- 6x6x5mm Tactile Push Buttons	2
- Male-to-Female Jumper Wires	6
- Breadboard	1
  
# Wiring:
- OLED / Button Pin	ESP32 Pin
- VCC	3.3V
- GND	GND
- SDA	(fill in your GPIO, e.g. GPIO21)
- SCL	(fill in your GPIO, e.g. GPIO22)
- Left button	(fill in GPIO) → GND
- Right button	(fill in GPIO) → GND

# Software Setup:

1. Arduino IDE setup
Install the ESP32 board package via Boards Manager if you haven't already.
Select your ESP32 Dev Module under Tools > Board.

2. Install libraries
Via Library Manager:
Adafruit_SSD1306
Adafruit_GFX (required by Adafruit_SSD1306)

4. Upload
Connect the ESP32 via USB.
Select the correct COM port under Tools > Port.
Upload DropCatch.ino.


# Game Logic Overview
- Paddle: horizontal position updated based on button state, moving left/right within the screen bounds.
- Circles: spawned at random x-positions at the top of the screen, fall at a fixed speed each frame.
- Collision detection: a circle is "caught" when its position overlaps the paddle's x-range at the paddle's y-position.
- Timer: a 30-second countdown starts when the game begins; game ends and final score displays when it hits zero.
- Score: increments by 1 for each circle caught; missed circles (reaching bottom of screen).















