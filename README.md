# Arduino-line-following-robot.Basic.
This Code is for Easy Arduino line following robot with 4 line sensing array.
     
     
    #define S1 2   //sensor1
    #define S2 3   //sensor2
    #define  S3 4 //sensor3
    #define S4 5    //sensor4
    #define LM1 7   //left motor pin
    #define RM1 8   //right motor pin
       

    void setup()
    {
    pinMode(S1, INPUT);
    pinMode(S2, INPUT);
    pinMode(S3, INPUT);
    pinMode(S4, INPUT);
    pinMode(LM1, OUTPUT);
    pinMode(RM1, OUTPUT);

    }
    void loop()
    {
     if(digitalRead(S2) && digitalRead(S3) && digitalRead(S1) &&digitalRead(S4))
     {
     digitalWrite(LM1, LOW);
     digitalWrite(RM1, LOW);
      }
  
    if(!(digitalRead(S3)) && (digitalRead(S2)))   
    {
    digitalWrite(RM1, HIGH);
    digitalWrite(LM1, LOW);
     }
  
    if(digitalRead(S3) && !(digitalRead(S2)))
    {
    digitalWrite(LM1, HIGH);
    digitalWrite(RM1, LOW);
     }
  
    if(!(digitalRead(S3)) && !(digitalRead(S2)) && !(digitalRead(S1)) && !(digitalRead(S4)))
    {
    digitalWrite(LM1, HIGH);
    digitalWrite(RM1, HIGH);
     }
    if( (digitalRead(S1)) )
    {
        digitalWrite(RM1,HIGH);
        digitalWrite(LM1,LOW);
    }
    if( (digitalRead(S4)))
    {
        digitalWrite(LM1,HIGH);
        digitalWrite(RM1,LOW);
        
     }
    
    
       }﻿
