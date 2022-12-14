def makeGrayscalePicture():
   file = pickAFile()                        
   pic = makePicture(file)
   
   # Now get each pixel in the image
   pixels = getPixels(pic)
   
   for pixel in pixels:
       # Get the R, G and B values from the pixels. 
       r = getRed(pixel)
       g = getGreen(pixel)
       b = getBlue(pixel)
       
       # Get the average color value for that pixel. 
       average = (r + g + b) / 3 
       
       # Set all the R, G and B values to the same value. This will make it grey.
       setRed(pixel, average)
       setGreen(pixel, average)
       setBlue(pixel, average)

   show(pic)
  

def makeNegativePicture():
   file = pickAFile()                        
   pic = makePicture(file)  
   
   # this gets all the pixels
   pixels = getPixels(pic) 
   
   # Go through each pixel and modify its color
   for pixel in pixels:
       # Get the current r, g and b values of the pixel
       r = getRed(pixel)
       g = getGreen(pixel)
       b = getBlue(pixel)
       
       # Get the opposite color values
       newRed = 255 - r
       newBlue = 255 - g
       newGreen = 255 - b
       
       # Set the new colors
       setRed(pixel, newRed)
       setBlue(pixel, newBlue)
       setGreen(pixel, newGreen)

   show(pic) 
   
def alterReds():
  file = pickAFile()                        
  pic = makePicture(file)  
   
  # this gets all the pixels
  pixels = getPixels(pic) 
  
  for pixel in pixels: 
    # Get the current red value of the pixel
    r = getRed(pixel) 
    
    # double the red value
    enhancedRed = r*2  	
    
    # Set the new pixel color
    setRed(pixel, enhancedRed)
    
  show(pic)

def mirror():
  file = pickAFile()                        
  pic = makePicture(file) 
  
  # Get the width and height of the picture 
  width = getWidth(pic)
  height = getHeight(pic)
  
  # Create an empty canvas to create the new mirrored picture
  mirroredPic = makeEmptyPicture(width*2, height)
  
  # For each x and y coordinate in the image
  for x in range(0, width):
    for y in range(0, height):
        # Get the original pixel
        originalPix = getPixel(pic, x, y)
        
        # Get the pixel on the left side of the new mirrored picture
        leftMirrorPixel = getPixel(mirroredPic, x, y)
        
        # Sets the colour of the left side to the original color
        setColor(leftMirrorPixel, getColor(originalPix))
        
        # Get the location of where we want to copy the pixel on the right side
        rightMirrorPixel = getPixel(mirroredPic, (width*2)-x-1, y)
                
        # Sets the colour of the right side to the mirrored pixel
        setColor(rightMirrorPixel, getColor(originalPix))
        
  show(mirroredPic)
  