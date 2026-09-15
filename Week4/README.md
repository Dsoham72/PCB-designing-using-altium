Regulator Choice: L7805CP (7805, TO-220)
Chosen for a fixed 5V output since all sensors on this board (MPU-6050, IR module, HC-SR04) run comfortably off 5V. Input is a 9V battery, giving enough headroom
above the 7-7.5V minimum input the 7805 needs to regulate cleanly.

Decoupling
- Regulator input: 0.33µF ceramic across IN/GND
- Regulator output: 0.1µF ceramic across OUT/GND
- One additional 0.1µF ceramic placed right at each sensor header

I2C Routing (MPU-6050)
Added 4.7kΩ pull-up resistors on SCL and SDA to 5V, in case the specific MPU-6050 breakout used doesn't already have onboard pull-ups.

Thermal Management
Added a ground-connected copper pour spanning the full board on the bottom layer.

Validation**
Design Rule Check run with 0 violations
