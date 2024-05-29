const int PB_1 = 2; // Button1
const int RLY_1 = 13; //relay 1
const int PB_2 = 3; // Button2
const int RLY_2 = 12; //relay 2
const int PB_3 = 4; // Button3
const int RLY_3 = 11; //relay 3

const int PB_4 = 5; // Button4
const int RLY_4 = 10; //relay 4

//VARIABLES
int buttonState1 = 0; 
    // current state of the button
bool relay1 = false;
int buttonState2 = 0; 
    // current state of the button
bool relay2 = false;

int buttonState3 = 0; 
    // current state of the button
bool relay3 = false;

int buttonState4 = 0; 
    // current state of the button
bool relay4 = false;

//MILLIS
unsigned long previousMillis1 = 0;
unsigned long previousMillis2 = 0;
unsigned long previousMillis3 = 0;
unsigned long previousMillis4 = 0;
const unsigned long interval1 = 20000;
const unsigned long interval2 = 20000;
const unsigned long interval3 = 20000;
const unsigned long interval4 = 20000;





void setup()
{
  pinMode(PB_1, INPUT);
  digitalWrite(PB_1, HIGH); // pull-up
  pinMode(PB_2, INPUT);
  digitalWrite(PB_2, HIGH); // pull-up
  pinMode(RLY_1, OUTPUT);
  digitalWrite(RLY_1, LOW);
  pinMode(RLY_2, OUTPUT);
  digitalWrite(RLY_2, LOW);

  
pinMode(RLY_3, OUTPUT);
  digitalWrite(RLY_3, LOW);

 pinMode(RLY_4, OUTPUT);
  digitalWrite(RLY_4, LOW); 
  
  Serial.begin(9600);
 }


void loop(){

    // read the pushbutton input pin:
    buttonState1 = digitalRead(PB_1);
    buttonState2 = digitalRead(PB_2);
    buttonState3 = digitalRead(PB_3);
    buttonState4 = digitalRead(PB_4);
    unsigned long currentMillis = millis();

    // Aqui voy bien !!!
    

    // if button is pressed, turn relay on (if it wasn't already on), and reset the timer
    if( buttonState1==HIGH ) // no need to check for previous state, in this specific case
    {
        previousMillis1 = currentMillis;
        digitalWrite(RLY_1, HIGH);
        
        relay1 = true;
    }

     if( relay1 )
    {
        // turn red led on, if close to turning off the relay
        
        // if enough time has elapsed, turn of the relay
        if (currentMillis - previousMillis1 >= interval1) 
        {
            // .. turn of relay
            digitalWrite(RLY_1, LOW);
            relay1 = false;
        }
    } 

if( buttonState2==HIGH ) // no need to check for previous state, in this specific case
    {
        previousMillis2 = currentMillis;
        digitalWrite(RLY_2, HIGH);
        
        relay2 = true;
    }

     if( relay2 )
    {
        // turn red led on, if close to turning off the relay
        
        // if enough time has elapsed, turn of the relay
        if (currentMillis - previousMillis2 >= interval2) 
        {
            // .. turn of relay
            digitalWrite(RLY_2, LOW);
            relay2 = false;
        }
    }
    //  Aqui el Final que me da problemas
    if( buttonState4==HIGH ) // no need to check for previous state, in this specific case
    {
        previousMillis3 = currentMillis;
        digitalWrite(RLY_3, HIGH);
        
        relay3 = true;
    }

     if( relay3 )
    {
        // turn red led on, if close to turning off the relay
        
        // if enough time has elapsed, turn of the relay
        if (currentMillis - previousMillis3 >= interval3) 
        {
            // .. turn of relay
            digitalWrite(RLY_3, LOW);
            relay3 = false;
        }

        //   aquuii
        if( buttonState4==HIGH ) // no need to check for previous state, in this specific case
    {
        previousMillis4 = currentMillis;
        digitalWrite(RLY_4, HIGH);
        
        relay4 = true;
    }

     if( relay4 )
    {
        // turn red led on, if close to turning off the relay
        
        // if enough time has elapsed, turn of the relay
        if (currentMillis - previousMillis4 >= interval4) 
        {
            // .. turn of relay
            digitalWrite(RLY_4, LOW);
            relay4 = false;
        }
    
    }
    }    } 
