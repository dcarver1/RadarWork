1/31/2018
Dan Carver
carver.dan1@gmail.com


Notes taken from ARSET webinar section 1
[link to first training ](https://arset.gsfc.nasa.gov/disasters/webinars/intro-SAR)

# General information
Radar is an active sensor that uses electromagnet radiation from the microwave range
microwaves are not effected by day/night or clouds

## Advantages
- very sensitive to dielectric properties and structure of the feature

## disadvantages
- topography alters the radar and it needs to be accounted for

## how it works
Imaging radar systems are all side looking. They function by measuring the difference in time between when the signal is sent and when the signal to returns to the sensor.

The intensity of the signal is measured as backscatter. The actual values range across orders of magnitudes which needs to be accounted when conducting certain statistics or comparisons
Return time is measured to calculate distance.

The resolution is determine based on the size of the antenna. Because large antennas are difficult to maintain in space they use the movement of the senor to synthetically increase the size of the antenna. Hence Synthetic Aperture Radar (SAR)

Radar measures amplitude and phase.
amplitude is the strength of the signal know as backscatter coefficient.

All SAR data contains information about
- Structure of the feature
- dielectric properties of the feature

Three instrument parameters  effect the return signal
1. Wavelength; distance between peaks of a wave
different wavelengths interact with the surfaces differently
longer wavelength have greater penetration.
if the wavelength is bout the same size as the object backscatter will occur. If the wavelength is smaller then the object the surface will appear smooth(low backscatter).

C Band is used on sentinel 1
C-Band is recommended for identifying structure of agricultural products
L-band is ideal in detecting inundated vegetation;

2. Polarization
polarization defines the orientation of the wavelength.
common notation
1st letter refers to the transmitted orientation, 2nd is received orientation
HH:
HV:
VH:
VV:
HH and VV are co-polarized
HV and VH are cross polarized

3. Incidence Angle
The angle between the sensor and Earth's surface plane
larger angles will be more sensitive to surface roughness
backscatter decreases with the lowering of incident angle

## Radar Backscatter
The amount of energy returned to the sensor is influenced by the three parameters above
The brightness of the image from radar is dependent on the intensity of the Backscatter
The higher the backscatter the brighter the image

**surface Roughness**
- the average height variation of the features on the surface.
- if average height is much smaller then wavelength the feature will appear smooth
- size and orientation influences the scattering
- different polarization combinations can detect differ structures

**dielectric constant** is a measure of conductivity
- presence of absence of moisture drives the dielectric constant
- water has a very high effect on the dielectric content
- reflectively increases with increase moisture content

## Reflection
- smooth water often appears as dark due to spectral reflectance
- volume scattering is indicative of vegetation
- double bounce; often show inundated vegetation.

## Geometric and Radiometric distortion
- slant range
resolution will vary across the image. Edges are compressed relative to the actual ground
This must be corrected if distance measurements are to be made with the image

- relief displacement
foreshortening: energy reaches the bottom of a slope before the top. This changes the slope of the object, it looks compressed
layover; energy reaches the top of a tall feature before it reaches the base. So the top is display before the base, hence layover.
relief displacement can be correct using a DEM

- radar shadowing
if energy can not reach areas, data gaps will be generated

- antenna pattern
the strength of a signal is more significant closer to the center of the swath
this can be correct to average out the values across the image.

## Speckel
grainy images are cause by random variability in reflectance from sub pixel objects. This variation results in a variance in backscatter between cells across a similar surface.

The amount of speckle can be reduce with
- multilook; split the beam into multiple features and average all the features.
comes at the cost of decreases resolution
- spatial filtering
Moving window to average out value from that window.
This smooth's the image

# SAR Processing and Data Analysis
[pdf of slides](https://arset.gsfc.nasa.gov/sites/default/files/disasters/SAR-17/Session2-SAR-English.pdf)

## objectives
1. using sentinel-1
2. performing image preprocessing
3. analyze SAR imagery to classify water

## sentinel1 background
both sentinel 1-A and 1-B have the same sensor characteristics; 6 day repeat
this goes over using snap for data processing
seem like snap has a good interface
[link to snap](http://step.esa.int/main/toolboxes/snap/)

This is really a step by step for the preprocessing tools. it looks like a great interface.
in the end they run an thresholding classification based on histograms to bin water and not water.

If you need to do Sentinal1 preprocessing this is a perfect resource
