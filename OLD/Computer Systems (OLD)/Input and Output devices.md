# Barcode Readers

#compsci
Barcode readers typically work on the principle of reflected light, light from a laser is directed at a pattern and a sensor detects the intensity of light that bounces back similar to [[Secondary storage devices#Optical storage|optical storage]]

There are two common types of barcode system:
- Universal Product Code (UPC-A) / European Article Number (EAN), this is commonly used in retail and warehousing.
-  ![](https://i.imgur.com/6IMLOEc.png)
- Code 128, this is used in transport and shipment tracking. Code 128 can represent letters and numbers whilst UPC-A and EAN can only represent numeric digits.
![](https://i.imgur.com/CoNICMj.png)

## UPC-A / EAN Systems

This uses long guard bars to show the start and end of the barcode and also a central guard bars to distinguish left uniquely from right.
![](https://i.imgur.com/YMmw6vp.png)

### Reading Retail Barcodes

A grouping of two or more adjacent bars appear as a single wide bar. Right hand codes are the inverse of left hand codes, left hand codes all have an odd number of black bars. Right hand codes all have an even number.

## QR (Quick Response) Codes

QR codes are 2D barcodes and can be read by smartphones or tablets

# Digital Cameras

A camera works in much the same way as a scanner, when a digital camera captures an image it breaks up what it sees through its lens into a grid of pixels.

### How a Camera Digital Camera Works

The shutter opens to let light onto a sensor at the back of the lens, the intensity of the light is measured by millions of tiny sensors (one per pixel) arranged in a grid on the sensor, Light levels for each pixel are represented as binary values which can then be stored in the camera's memory

### Sensing Colour

Red green or blue filters are used with different sensors in the camera to separate out these wavelengths, the intensity of each of these colours falling on the sensors is measured and stored to aggregate an RGB value.

# Laser Printers

Laser printers use dry powdered ink called toner
- A print drum is given a negative static charge
- A laser shines a reverse image of page at the drum
- Laser light reverses the charge or the drum
- Toner is charged negatively and sticks to positively charged image
- Toner is transferred from drum to paper and fused using a heat roller
- ![](https://i.imgur.com/X73sbh3.png)

# Radio Frequency ID (RFID)

RFID systems use a transponder and a receiver
- The powered receiver emits radio frequency energy
- The transponder antenna in the bank card, mobile phone or tag becomes energised by radio waves
- The transponder can then send data to the receiver
RFID tags are used in many places such as security control points or supply chain tracking for goods.

## Passive and Active Tags

Passive transponders used in bank cards for example have no power source themselves and rely on radio waves from the receiver. Active tags use a larger, battery powered beacon which can broadcast its own signal.