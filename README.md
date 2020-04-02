# Verkefni-4-VESM2
### Verkefni 4 (5%)

**Að Láta tvo Arduino tala saman með I2C**
 
1. Skoðaðu eftirfarandi skýringarmyndband og tutorial [I2C Part 1 - Using 2 Arduinos](https://www.youtube.com/watch?v=PnG4fO5_vU4&list=PLWNDWPAClRVpetVqItj-TC0vsflLzN9-8&index=2&t=355s). Settu upp tilraunirnar báðar í Tinkercad.

2. Lestu greinina [How to use I2C in Arduino: Communication between two Arduino Boards](https://circuitdigest.com/microcontroller-projects/arduino-i2c-tutorial-communication-between-two-arduino) og settu upp í Tinkercad.

Athuga, það þarf að bæta við tveimur línum í kóðann sem er í greininni, línurnar eiga að koma á milli `byte SlaveReceived = 0` og `void setup()` ofarlega í kóðanum fyrir Slave (þarf ekki í kóðann fyrir Master):

  ```c
  byte SlaveReceive = 0; // <--- Þessi lína er þegar til staðar.
  void receiveEvent(int); // <--- Bæta þessari línu við.
  void requestEvent(); // <--- Bæta þessari línu við.
  void setup() // <--- Þessi lína er þegar til staðar.
  ```
   * #### [Svar fyrir Tinkercadverkefni 1](https://www.tinkercad.com/things/bQXNtgzwLia-i2c-part-1-using-2-arduinos/editel)
   * #### [Svar fyrir Tinkercadverkefni 2](https://www.tinkercad.com/things/8XvAzjj6vo7-smashing-snaget/editel)

3. Fáðu allt til að virka og svaraðu svo eftirfarandi spurningum:
 
   1. Hvað er átt við með samstilltum (e. synchronous) samskiptastaðli?
      * __Svar:__ Það á við að tveir eða fleiri skiptast á upplýsingum í rauntíma. Á flestum vinnustöðum gerast samskipti þannig og fólk býst við svörum í rauntíma. Vandinn við þessa nálgun er að hún er í raun ekki mjög árangursrík.
   2. Hver er munurinn á SDA og SCL?
      * __Svar:__ SCL er klukkumerkið og SDA er gagnamerkið. Klukkumerkið er alltaf búið til af núverandi tengimeistara; sum þræla-tæki geta þvingað klukkuna lítið stundum til að seinka meistaranum að senda fleiri gögn (eða þurfa meiri tíma til að undirbúa gögn áður en meistarinn reynir að loka fyrir þeim).
   3. Í Master kóðanum er línan `Wire.begin();` og í Slave kóðanum er sambærileg lína `Wire.begin(8);`.
      1. Hvað þýðir talan 8 í Slave kóðanum?
         * __Svar:__ Byrjar I2C samskipti við Slave Address sem 8 á pinna (A4, A5)
      2. Hvað þýðir að það er engin tala í Master kóðanum?
         * __Svar:__ Byrjar I2C samskipti við pinna (A4, A5)
      
4. Stafrænt hallamál. Horfðu á [Build a Digital Level with MPU-6050 and Arduino](https://www.youtube.com/watch?v=XCyRXMvVSCw) myndbandið til enda. Fylgdu eftir **fyrri** tilrauninni sem er í myndbandinu og settu upp verklega. Sjá einnig [vefgrein](https://dronebotworkshop.com/mpu-6050-level/). Ef þú ert ekki með MPU-6050 eða hann er ólóðaður gerðu þá [þetta verkefni í staðinn](https://gist.github.com/gestskoli/c807f6f4f310a2255fd59d1bffa8eddc)
   * [Svar fyrir verklegt en án ólóðað MPU-6050]()

5. Valkvæmt (ekki til einkunna). Skoðaðu [MPU6050 and 3D Simulation With Processing](https://www.instructables.com/id/Arduino-MPU6050-GY521-6-Axis-Accelerometer-Gyro-3D/)

### Námsmat og skil
Gefið er heilt fyrir fullnægjandi lausnir og svör, hálft ef ábótavant eða svör vanta.

Skilaðu á Innu vefslóð á Github wiki vefsíðu sem inniheldur:

1. Tinkercad tengla á báðar lausnir úr lið 1. 
2. Tinkercad tengil á lausn úr lið 2. 
3. Svör við spurningum úr lið 3.
4. Tengil á myndband af virkni úr lið 4.


