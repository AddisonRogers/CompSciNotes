For n number of bits there are 2^n possible combinations.

A computer often has to store and process real-world data. A computer needs data in a format it can understand : patterns of 1s and 0s. This type of data is referred to as digital data. It is different from analogue data which can in theory be measured to any degree of accuracy. 

## Images
Humans see 'images' by detecting the light reflected by objects they are looking at. Light is transmitted as waves and changing wave lengths produce different colours. 

When a digital camera captures the image it breaks up what it sees through its lens into a grid of pixels.
- A light sensor measures the intensity of colour in each pixel
- Each measurement is converted into a binary code using an electronic component called analogue-to-digital converter
- The number of pixels recorded in the grid affects the number of bits used and, therefore, the size of the file created.

## Bitmap Graphics
Bit-mapped graphics are created using a grid of pixels. each pixel is given a colour value.
Common bitmap file types are : 
- BMP 
- JPG
- GIF
- PNG
- TIF
The number of pixels used to make up a bitmap image is defined by the resolution. The area is defined by the image width and height in pixels ie 1080 * 1920.

Resolution is defined as width x height. Resolution doesn't define the actual physical size of the image however, every image can be infinitely grown or shrink however you can suffer from deterioration in quality. 

### Creating an image
Each pixel is given a binary value. Each value represents a different colour. Each pixel can represent a finite number of colours. 2^n dictates the bit depth and the number of colours that can be represented. A higher bit depth gives a greater range of colour and a better quality of image. 

### Calculating file size
Image file size is determined by the number of pixels used and then umber of colour combinations available. Ie 2 megapixels x 24 bit colour depth = 2,000,000 x 24

Quality is traded off against file size - you cant have high quality and low file size.

### Metadata
Metadata is data about data and is stored in the same file as the image data. It includes:
- The date it was created
- The width and height in pixels of the image
- The colour depth
- The GPS coordinates of where a photo was taken

## Vector graphics
Vector images are made up of geometric shapes or objects rather than by manipulating individual pixels. The properties of each shape are stored and retrieved in order to mathematically redraw the shape on the screen to display it.
Common file formats :
- SWF
- EPS
- SVG

The properties of shapes are stored in a vector drawing list to define them. These include:
- Shape type and position on screen
- Fill colour
- Line colour and weight
- Length and width or radius

Common software functions can be used to set or adjust these properties.
Vector graphics are typically larger,but do not lose quality as it grows.

## Resizing images
Whilst bitmap graphics will often pixelate as you enlarge them, vectors are mathematically redrawn at whatever size they are set to.