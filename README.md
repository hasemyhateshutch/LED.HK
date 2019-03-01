#include <FastLED.h>

#define NUM_LEDS 135
#define DATA_PIN 11

CRGB leds[NUM_LEDS];
int cycles = 5;
int speed = 10;


void setup(){
  FastLED.addLeds<WS2812B, DATA_PIN, GRB>(leds, NUM_LEDS);

  }

void loop(){  
    if(cycles == 0 ){
      for(int i = 0; i< NUM_LEDS; i++){
        
       leds[1-20] = CRGB::Red;
       leds[21-41] = CRGB::Orange;
       leds[42-62] = CRGB::Green;
       leds[63-83] = CRGB::Aqua;
       leds[83-103] = CRGB::Blue;
       leds[104-123] = CRGB::Purple;
       leds[124-135] = CRGB::Pink;

        delay(400); 
      }
    }
        for(int j = 0; j<256*cycles; j++){
      for (int q = 0; q < 3; q++){
        for(int i = 0; i <NUM_LEDS; i=i+3){
          int pos = i+q;
          
      leds[1-20] = CRGB::Red;
      leds[21-41] = CRGB::Orange;
      leds[42-62] = CRGB::Green;
      leds[63-83] = CRGB::Aqua;
      leds[83-103] = CRGB::Blue;
      leds[104-123] = CRGB::Purple;
      leds[124-135] = CRGB::Pink;
   
         }
         FastLED.show();

         delay(400);
         for (int i = 0; i<NUM_LEDS; i=i+3){
         }
       }
     }
    }
