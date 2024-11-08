#include <SoftwareSerial.h>

int sensorPin = A0;
int sensorValue = 0;
int led = 3;
void setup(){
  pinMode(led, OUTPUT);
  Serial.begin(9600);}
  void loop()
{
  Serial.println(" Automatice street  light using LED & LDR System");
  sensorValue = analogRead(sensorPin);
  Serial.println(sensorValue);
  if (sensorValue < 100)
  
{
  Serial.println("LED LIGHT ON");
  digitalWrite(led,HIGH);
  delay(500);
}
digitalWrite(led,LOW);
delay(500);

}
