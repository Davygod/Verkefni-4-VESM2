# Verkefni-4-VESM2
### Verkefni 4 (5%)

**Að Láta tvo Arduino tala saman með I2C**
 
1. Skoðaðu eftirfarandi skýringarmyndband og tutorial [I2C Part 1 - Using 2 Arduinos](https://www.youtube.com/watch?v=PnG4fO5_vU4&list=PLWNDWPAClRVpetVqItj-TC0vsflLzN9-8&index=2&t=355s). Settu upp tilraunirna báðar í Tinkercad.

2. Lestu greinina [How to use I2C in Arduino: Communication between two Arduino Boards](https://circuitdigest.com/microcontroller-projects/arduino-i2c-tutorial-communication-between-two-arduino) og settu upp í Tinkercad.

Athuga, það þarf að bæta við tveimur línum í kóðann sem er í greininni, línurnar eiga að koma á milli `byte SlaveReceived = 0` og `void setup()` ofarlega í kóðanum fyrir Slave (þarf ekki í kóðann fyrir Master):

  ```c
  byte SlaveReceive = 0; // <--- Þessi lína er þegar til staðar.
  void receiveEvent(int); // <--- Bæta þessari línu við.
  void requestEvent(); // <--- Bæta þessari línu við.
  void setup() // <--- Þessi lína er þegar til staðar.
  ```
  
   * #### [Svar fyrir Tinkercadverkefnið](https://www.tinkercad.com/things/8XvAzjj6vo7-smashing-snaget/editel)

3. Fáðu allt til að virka og svaraðu svo eftirfarandi spurningum:
 
   1. Hvað er átt við með samstilltum (e. synchronous) samskiptastaðli?
   2. Hver er munurinn á SDA og SCL?
   3. Í Master kóðanum er línan `Wire.begin();` og í Slave kóðanum er sambærileg lína `Wire.begin(8);`.
      1. Hvað þýðir talan 8 í Slave kóðanum?
      2. Hvað þýðir að það er engin tala í Master kóðanum?
      
 4. (Væntanlegt!)
