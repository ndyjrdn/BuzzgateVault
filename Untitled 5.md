```
//sonic distance sensor
int trig = 12;
int echo = 11;
float distance;
float time;

void setup()
{
  pinMode(trig, OUTPUT);
  pinMode(echo, INPUT);
  Serial.begin(9600);
}

void loop()
{
 digitalWrite(trig, LOW);
 delayMicroseconds(2);
 digitalWrite(trig, HIGH);
 delayMicroseconds(10);
 digitalWrite(trig, LOW);
 time = pulseIn(echo, HIGH); //time from line ll to when it hears
 distance = time*148.1; //distance in inches
 Serial.println(distance);
}
```


```
//gearbox forward and backward
int motorPin1 = 10, motorPin2 = 11;

void setup()
{
  pinMode(motorPin1, OUTPUT);
  pinMode(motorPin2, OUTPUT);
}

void loop()
{
  digitalWrite(motorPin1, HIGH);
  digitalWrite(motorPin2, LOW);
  delay(1000);
  digitalWrite(motorPin1, LOW);
  digitalWrite(motorPin2, LOW);
  delay(1000);
  digitalWrite(motorPin1, LOW);
  digitalWrite(motorPin2, HIGH);
  delay(1000);
}
```