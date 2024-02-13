# arduino-animatronic-skull
Code (sketch) for random movements in an animatronic skull, using an arduino clone (attiny88) and sg90 microservos.

In this project i use three sg90 micro servos in a servo arrangement of three objects of the Servo class: servo[0] for the jaw, and servo[1] and servo[2] interchangeably for the neck of the skull, which we manage with random movements in each of them, using the randomseed function, and using as a parameter for said function, the electrical noise captured in the analog pin A0: this will ensure a series of different and unrepeatable movements every time we turn on the attiny88. I did the park sub routine -estacionar(Servo servo, byte angFin)- to place the servos in a starting position by activating and deactivating with the switch -pinMode(3, INPUT_PULLUP)-, thus avoiding sudden movements every time we use it. 

You can see how the animatronic works in this video: www.youtube.com/watch?v=6xGNQlUAutQ
