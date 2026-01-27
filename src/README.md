Arduino source code placed here.







char data; // Variable to store received data

void setup() {
  Serial.begin(9600); // Start serial communication at 9600 baud rate

  // Set motor control pins as output
  pinMode(7, OUTPUT); 
  pinMode(6, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(4, OUTPUT);

}

void loop() {
  if (Serial.available() > 0) {
    data = Serial.read(); // Read received data

    // Control motor movement based on received data
    switch (data) {
      case 'F': // Move Forward
        digitalWrite(7, HIGH);
        digitalWrite(6, LOW);
        digitalWrite(5, HIGH);
        digitalWrite(4, LOW);
        break;
      case 'B': // Move Backward
        digitalWrite(7, LOW);
        digitalWrite(6, HIGH);
        digitalWrite(5, LOW);
        digitalWrite(4, HIGH);
        break;
      case 'R': // Turn Left
        digitalWrite(7, LOW);
        digitalWrite(6, HIGH);
        digitalWrite(5, HIGH);
        digitalWrite(4, LOW);
        break;
      case 'L': // Turn Right
        digitalWrite(7, HIGH);
        digitalWrite(6, LOW);
        digitalWrite(5, LOW);
        digitalWrite(4, HIGH);
        break;
      case 'S': // Stop
        digitalWrite(7, LOW);
        digitalWrite(6, LOW);
        digitalWrite(5, LOW);
        digitalWrite(4, LOW);
        break;
    }
  }
}
