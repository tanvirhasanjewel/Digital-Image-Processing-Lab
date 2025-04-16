## Digital Image Processing Lab
- **[Audity Ghosh](https://github.com/AudityGhosh)**
- **University of Information Technology and Sciences (UITS)**

### Lab Tasks
- **Task 1: The primary objectives of this lab session are: Understanding image processing operations in Python. Extracting a specific region from an image. Converting an image to the HSV color space and analyzing its components. -**
	- **(a) Extracting a 100×100 Region from the Center of an Image, Load an image from a given URL. Determine the center coordinates of the image. Extract a 100×100 pixel region from the center. Display both the original and cropped image for comparison. ✓**
	- **(b) Converting an Image to HSV and Visualizing Components, Convert the input image from RGB to HSV color space. Extract and visualize the Hue, Saturation, and Value components individually in grayscale. Analyze how HSV representation differs from RGB.✓**
   
- **Task 2: This lab assignment aims to implement multiple image transformation techniques using Python and OpenCV. The transformations include resizing, rotating, and flipping an image, followed by displaying all results in a single plot. –**
	- **(a) Resize an Image: Resize the image to 256x256 pixels. ✓**
	- **(b) Rotate by 180 Degrees (Clockwise): Rotate the image by 180 degrees in the clockwise direction. ✓**
	- **(c) Vertical Flip: Flip the image vertically. ✓**
 	- **(d) Display Transformations: Display the original image and all transformed images in a 2x2 subplot for comparison. ✓**
   
- **Task 3: Create two 400x400 images with black background  –**
	- **(a) The first image should contain a green rectangle at the center. ✓**
	- **(b) The second image should contain a magenta circle at the center. ✓**
	- **(c) Bitwise AND (cv2.bitwise_and): Show the overlapping region of the two images. ✓**
	- **(d) Bitwise OR (cv2.bitwise_or): Combine both shapes while retaining their colors. ✓**
 	- **(e) Bitwise XOR (cv2.bitwise_xor): Retains only the non-overlapping parts of both images. ✓**
  	- **(d) Bitwise NOT (cv2.bitwise_not): Inverts the colors of each shape separately. ✓**
  	- **(f) Element-wise Multiplication (cv2.multiply): Observe the effect on overlapping areas. ✓**
  	- **(g) Alpha Blending (cv2.addWeighted): Blend both images with transparency effects. ✓**
  	- **(h) Image Subtraction (cv2.subtract): Highlights the differences between the two images. ✓**
   
- **Task 4: Read a black and white image using URL and apply this custom weighted filter on that image (both manually and using cv2.filter2D) and show all 3 pictures in the same plot as subplots. –**
	- **(a) It is normalized by dividing by the sum of its weights (10) to preserve brightness. The custom filter used is: ✓**
 - [ 1 1 1 ]
 - [ 1 2 1 ]
 - [ 1 1 1 ]
 
