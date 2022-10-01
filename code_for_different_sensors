Code:
#include"DHT.h"
#define DHTPIN 2 //Digital pin connected 
to the DHT sensor
#define DHTTYPE DHT11 //DHT 11
//for moisture sensing in soil
const int moistureA0=0;
int AO=0;
int tmp=0;
//int buzzPin=11;
int LED=13;
DHT dht(DHTPIN, DHTTYPE);
void setup() 
{
 Serial.println(9600);
 Serial.println("Soil moisture sesnor");
 pinMode(moistureA0,INPUT);
 //pinMode(buzzPin,OUTPUT) //SET PIN AS 
OUTPUT
 pinMode(LED,OUTPUT);//SET PIN AS OUTPUT
 //for dht11 sensor
 Serial.begin(9600);
 Serial.println(F("DHTxx test!"));
 dht.begin();
}
 void loop()
{
 //for checking humidity ,temperature ,heat 
index
 // Wait a few seconds between 
measurements.
 delay(2000);
 // Reading temperature or humidity takes 
about 250 milliseconds!
 // Sensor readings may also be up to 2 
seconds 'old' (its a very slow sensor)
 float h = dht.readHumidity();
 // Read temperature as Celsius (the 
default)
 float t = dht.readTemperature();
 // Read temperature as Fahrenheit 
(isFahrenheit = true)
 float f = dht.readTemperature(true);
 // Check if any reads failed and exit 
early (to try again).
 if (isnan(h) || isnan(t) || isnan(f)) {
 Serial.println(F("Failed to read from 
DHT sensor!"));
 return;
 }
 // Compute heat index in Fahrenheit (the 
default)
 float hif = dht.computeHeatIndex(f, h);
 // Compute heat index in Celsius
(isFahreheit = false)
 float hic = dht.computeHeatIndex(t, h, 
false);
 Serial.print(F(" Humidity: "));
 Serial.print(h);
 
 Serial.print(F("% Temperature: "));
 Serial.print(t);
 
 Serial.print(F("C "));
 Serial.print(f);
 
 Serial.print(F("F Heat index: "));
 Serial.print(hic);
 
 Serial.print(F("C "));
 Serial.print(hif);
 
 Serial.println(F("F"));
 
 tmp=analogRead(moistureA0);
 if(tmp!=A0)
 {
 AO=tmp;
 Serial.print("A="); //show resistance 
value of the sensor in the IDE
 
 Serial.println(A0); 
 }
 delay(1000);
 if(analogRead(0)>900). //if reading is 
higher than 900
 {
 //digitalWrite(buzzPin,HIGH); //the 
buzzer will sound 
 digitalWrite(LED,HIGH); //the led will 
light
 delay(1000);
 //digitalWrite(buzzPin,LOW);
 digitalWrite(LED,HIGH);
 }
 Else
 {
 // digitalWrite(buzzPin,LOW);
 digitalWrite(LED,LOW);
 }
}
