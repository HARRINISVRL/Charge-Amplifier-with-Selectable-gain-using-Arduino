#include <stdio.h>
#include <stdlib.h>

float Dout, Din;
float number;
String receivedHex, Hex;

void setup() {
  Serial.begin(9600);
  pinMode(A7, INPUT);
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  digitalWrite(LED_BUILTIN, LOW);
}

void loop() {
  if (Serial.available() > 0) {
    receivedHex = Serial.readStringUntil('\n');
    Din = analogRead(A7);
    Dout = ((Din * 5.0 / 1023.0));

    if (receivedHex == "Vout") {
      Serial.print("t1.txt=\"");
      Serial.print(Dout);
      Serial.print(" V");
      Serial.print("\"");
      Serial.write(0xff); Serial.write(0xff); Serial.write(0xff);
    }

    if (receivedHex == "input") {
      Serial.print("t1.txt=\"");
      Serial.print(Dout);
      Serial.print(" V");
      Serial.print("\"");
      Serial.write(0xff); Serial.write(0xff); Serial.write(0xff);
      
      delay(5000);
      if (Serial.available() > 0) {
        String str = Serial.readString();
        if (str != "input") {
          number = str.toFloat();
          float gain = Dout / number;
          Serial.print("t6.txt=\"");
          Serial.print(gain);
          Serial.print("\"");
          Serial.write(0xff); Serial.write(0xff); Serial.write(0xff);
        }
      }
    }

    if (receivedHex == "gain") {
      delay(3000);
      if (Serial.available() > 0) {
        Hex = Serial.readString();
        if (Hex == "1") {
          digitalWrite(2, HIGH); digitalWrite(3, LOW); digitalWrite(4, LOW); digitalWrite(5, LOW);
        } else if (Hex == "2") {
          digitalWrite(3, HIGH); digitalWrite(2, LOW); digitalWrite(4, LOW); digitalWrite(5, LOW);
        } else if (Hex == "3") {
          digitalWrite(4, HIGH); digitalWrite(2, LOW); digitalWrite(3, LOW); digitalWrite(5, LOW);
        } else if (Hex == "4") {
          digitalWrite(5, HIGH); digitalWrite(2, LOW); digitalWrite(3, LOW); digitalWrite(4, LOW);
        }
      }
    }
  }
}
