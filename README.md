# codetech-task1
COMPANY: CODTECH IT SOLUTIONS

NAME:KUNDRAPU PAVAN KUMAR

INTERN ID:CT04DF2138

DOMAIN: Embedded Systems

DURATION: 4 WEEKS

MENTOR: Neela Santhosh Kumar# codetech-task-1

DESCRIPTION: The Push Button Counter is a simple embedded systems project where a digital counter increases each time a button is pressed. It uses a microcontroller like Arduino to read the push button input and display the count on an LCD or OLED screen. A pull-down resistor is used to ensure stable input readings. Debouncing is implemented in code to prevent false triggering. This project helps in understanding digital input, output display interfacing, and basic programming logic. It is commonly used in applications like people counters, product counting systems, and digital scoreboards. It’s an ideal beginner-level project in electronics.

CIRCUIT DIAGRAM: ![pushh](https://github.com/user-attachments/assets/620c4e23-9288-498c-bc41-d31b20334377)
CODE: #include <LiquidCrystal.h>

// LCD pins: RS, E, D4, D5, D6, D7 LiquidCrystal lcd(7, 8, 9, 10, 11, 12);

const int buttonPin = 2; int counter = 0; int buttonState = 0; int lastButtonState = 0;

void setup() { pinMode(buttonPin, INPUT); lcd.begin(16, 2); lcd.print("Counter: "); lcd.setCursor(0, 1); lcd.print(counter); }

void loop() { buttonState = digitalRead(buttonPin);

if (buttonState == HIGH && lastButtonState == LOW) { counter++; lcd.setCursor(0, 1); lcd.print(" "); // Clear line lcd.setCursor(0, 1); lcd.print(counter); delay(200); // Debounce delay }

lastButtonState = buttonState; }

OUTPUT:
![image](https://github.com/user-attachments/assets/5d01a1d5-0f5c-46e0-8463-ff3675dff07e)
WORKING DEMO:

https://youtu.be/hIQgd8ydFac?si=n8fogsGnqSqnytBo
