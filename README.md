const int ledPin = 9;   // use a PWM pin (3,5,6,9,10,11 on Uno)

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  // Increase brightness: 0 -> 255
  for (int brightness = 0; brightness <= 255; brightness++) {
    analogWrite(ledPin, brightness);  // set LED brightness
    delay(10);                        // small delay to see the fade
  }

  // Decrease brightness: 255 -> 0
  for (int brightness = 255; brightness >= 0; brightness--) {
    analogWrite(ledPin, brightness);
    delay(10);
  }

  // Then loop() repeats: continuous breathing effect
}
