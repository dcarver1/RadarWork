1/31/2018

Notes taken from ARSET webinar section 1
Notes from section 2 are below as well
[link](https://arset.gsfc.nasa.gov/disasters/webinars/intro-SAR)

# General information
Radar uses microwaves
microwaves are not effected by day/night or clouds

Active remote sensing in the microwave range is call radar

## Advantages
- very sensitive to dielectric properties and structure of the feature

## disadvantages
- topography alters the radar and it needs to be accounted for

## how it works
Imaging radar are all side looking because they function my measure the difference in time for a signal to return

Intensity is measure as backscatter
Time is measure for distance.

The resolution is determine based on the size of the antenna. Because large antennas are difficult to maintain in space they use the movement of the senor to synthetically increase the size of the antenna. Hence Synthetically Aperture Radar (SAR)

Radar measure amplitude and phase.
amplitude is the strength of the signal know as backscatter coefficient.

All SAR data contains information about
- Structure
- dielectric properties of the ground surface

Three instrument paraments effect this signal
1. Wavelength; distance between peaks of a wave
there area common radar bands. C  Band
different wavelength interact with the surface different
long wavelength have greater penetration.
if the wavelength is bout the same size as the object backscatter will occur. If the wavelength is smaller then the object the surface will appear smooth.
C=Band is recommended for identifing ag structure
L-band is ideal in detecting inundated vegetation; standing water under vag

2. Polarlization
polarization defines the orientation of the wavelength.
common notation
1st is transmitted, 2nd is received
HH:
HV:
VH:
VV:
HH and VV are light polarized
HV and VH are cross polarized

3. Incidence Angle
The angle of between the sensor and earth surface plane
large anlge will be more sensitve to surface roughness
back scatter descreses with lowering of incident angle

## Radar Backscatter
influce by the three parameters above

The brightness of the image from radar is dependent on the intensity of the Backscatter
Ground structure and dielectric content

** surface Roughness **
the avg height variation of the features on the surface.
if avg height is much smaller then wavelength the feature will appear smooth
size and orientation influences that scattering and this where polorization comes in to play
Dense scatters
dielectric constant measure of conductivity
- presence of absence of moisture drive the dielectric constant
- water has a very high effect on the dieletric content and
- reflectively increase with increase moisture content

## Reflection
- smooth water often appears as dark due to spectural refectance. mirror
- low veg areas are often rought surface reflectance.
- volume scattering is indicative of vegetation
- double bounce; often show inundated vegetation.

## Geometric and Radiometric distortion
- slant range
the image has a varying scale across the image. Edges are compressed relative to the actual ground
This must be corrected if distinct measurement are to be made with the image

- releif displacement
foreshortening: reaches the bottom of a slope before the top. This changes the slope of the object, it looks compressed
layover; reach top of a tall feature  before it reaches the base. So the top is display before the base, hence layover.

correct using a DEM

- radar shadowing
energey can not reach areas,create data gaps

- antenna pattern
strength of single is more significant the close to the center of the swatch
can be correct to average out the values across the image.

- topography does effect the process a lot. corrections needs to be made as a result.

## Speckel
grainy images; cause by random reflectance form sub pixel objects. This variation results in a variance between backscatter effect between cells acros a similar image.

can improve with
- multilook; split the beam into multiple features and average all the features.
comes at the cost of decreases resolution
- spatial filtering
Moving window to average out vaue from that window.
This smooths the image

ARSET section two

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

in the end they run an thresholding classification based on histograms to bin water and not water. They do not
