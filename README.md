#🔌 3-Input 3-Output Arduino Project
This is a simple Arduino-based circuit with 3 push buttons and 3 LEDs designed in Tinkercad Circuits. Each button controls one LED.

#🌐 Tinkercad Link
👉 [Click here to view the project](https://www.tinkercad.com/things/j2grzfGeZDa-brave-stantia-jofo)  

#🛠️ How It Works
The circuit includes 3 buttons as inputs and 3 LEDs as outputs.

When a button is pressed, it sends a LOW signal to the Arduino.

The Arduino then sets the corresponding output to LOW, turning the LED off.

When the button is not pressed, the input is HIGH, so the Arduino sends HIGH to the LED, turning it on.

This behavior simulates a simple digital control system where the button state directly controls the LED.

#🔢 Components Used
1x Arduino Uno

3x Push Buttons

3x LEDs (Red, Green, Blue)

3x Resistors (220Ω)

1x Breadboard

Jumper Wires


#💡 Arduino Code
 int buttonPin = 2;
int ledPin = 13;
int buttonState = 0;

int buttonPin2 = 1;
int ledPin2 = 12;
int buttonState2 = 0;

int buttonPin3 = 0;
int ledPin3 = 11;
int buttonState3 = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  
  pinMode(buttonPin2, INPUT);
  pinMode(ledPin2, OUTPUT);

  pinMode(buttonPin3, INPUT);
  pinMode(ledPin3, OUTPUT);
}

void loop() {
  buttonState = digitalRead(buttonPin);
  buttonState2 = digitalRead(buttonPin2); 
  buttonState3 = digitalRead(buttonPin3);

  digitalWrite(ledPin, buttonState);
  digitalWrite(ledPin2, buttonState2);
  digitalWrite(ledPin3, buttonState3);
}
