# moving-2-wheels

```
int inp1 = 32;
int inp2 = 33;
int inp3 = 31;
int inp4 = 30;
int enb1 = 2;
int enb2 = 3;


void moveForward(int speed) {
  digitalWrite(inp1, LOW);
  digitalWrite(inp2, HIGH);
  digitalWrite(inp3, HIGH);
  digitalWrite(inp4, LOW);
  analogWrite(enb1, speed);
  analogWrite(enb2, speed);
  Serial.println("Moving forward");
  // delay(duration*1000);
}

void moveBack(int speed, unsigned long duration) {
  digitalWrite(inp1, HIGH);
  digitalWrite(inp2, LOW);
  digitalWrite(inp3, LOW);
  digitalWrite(inp4, HIGH);
  analogWrite(enb1, speed);
  analogWrite(enb2, speed);
  Serial.println("Moving back");
  delay(duration*1000);
}

void moveRight(int speed, unsigned long duration) {
  digitalWrite(inp1, LOW);
  digitalWrite(inp2, HIGH);
  digitalWrite(inp3, LOW);
  digitalWrite(inp4, HIGH);
  analogWrite(enb1, speed);
  analogWrite(enb2, speed);
  Serial.println("Moving Right");
  delay(duration*1000);
}

void moveLeft(int speed, unsigned long duration) {
  digitalWrite(inp1, HIGH);
  digitalWrite(inp2, LOW);
  digitalWrite(inp3, HIGH);
  digitalWrite(inp4, LOW);
  analogWrite(enb1, speed);
  analogWrite(enb2, speed);
  Serial.println("Moving left");
  delay(duration*1000);
}

void stopMotors(unsigned long duration) {
  analogWrite(enb1, 0);
  analogWrite(enb2, 0);
  Serial.println("Stop");
  delay(duration*1000);
}


void setup() {
  pinMode(inp1, OUTPUT);
  pinMode(inp2, OUTPUT);
  pinMode(inp3, OUTPUT);
  pinMode(inp4, OUTPUT);
  pinMode(enb1, OUTPUT);
  pinMode(enb2, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  moveForward(200);
  delay(80); // push start

  moveForward(150);
  delay(1009.8);
  stopMotors(1);


  Serial.println("finish");
  delay(10000);
}

```
