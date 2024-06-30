Image Beautification Using Frequency Techniques
Introduction
The objective of this assignment was to enhance the visual quality of a set of images by 
applying image beautification techniques. The primary focus was on making the skin appear 
smoother and brighter, using frequency domain techniques combined with additional 
spatial domain enhancements. The images were processed to highlight the improvements 
before and after beautification.
Description of Algorithms and Methods
1. Image Preprocessing
- Reading Images: The input images were read from a specified directory. The images were in 
PNG format and included filenames such as '00.png', '01.png', etc.
- Color Space Conversion: Each image was converted from the BGR color space (default in 
OpenCV) to the RGB color space to ensure consistent processing and display.
2. Frequency Domain Processing
- Channel Separation: Each color channel (Red, Green, Blue) of the image was separated for 
individual processing.
- Fast Fourier Transform (FFT): The FFT was applied to each channel to convert the image 
data from the spatial domain to the frequency domain. This allowed for the manipulation of 
frequency components directly.
- Low-Pass Filtering: A circular mask was applied in the frequency domain to retain lowfrequency components while removing high-frequency noise. The radius of the mask was 
carefully chosen to balance between smoothing and preserving important details.
- Inverse FFT: The processed frequency data was transformed back to the spatial domain 
using the inverse FFT, resulting in a smoother version of the original image.
3. Skin Smoothing and Brightening
- Bilateral Filter: A bilateral filter was applied to the processed image to further smooth the 
skin while preserving edges. This filter helped in maintaining the natural look of facial 
features.
- Brightness Adjustment: The image was converted to the LAB color space, which separates 
the lightness component (L) from the color components (A and B). By increasing the Lchannel, the overall brightness of the skin was enhanced. The image was then converted 
back to the RGB color space.
4. Detail Enhancement
- Sharpening Filter: A sharpening filter was applied to the final processed image to enhance 
details and reduce any residual blurriness. This filter improved the clarity of facial features 
and other important details.
5. Saving and Visualization
- Saving Enhanced Images: The original and enhanced images were saved in separate 
directories ('before_beautification' and 'after_beautification'). This facilitated easy 
comparison and evaluation of the enhancements.
- Visual Comparison: Before and after images were displayed side-by-side using matplotlib 
to provide a clear visual representation of the improvements.
Results
The results of the image beautification process are presented below. Each pair of images 
shows the original image (left) and the enhanced image (right).
Image 00.png:
Image 01.png:
Image 02.png:
Image 03.png:
Image 04.png:
Image 05.png:
Discussion
The results of the image beautification process showed significant improvements in the 
appearance of the skin in the processed images. The frequency domain techniques 
effectively reduced noise and smoothed the skin texture. The bilateral filter and brightness 
adjustments further enhanced the visual quality by making the skin appear brighter and 
more even-toned.
The sharpening filter successfully mitigated any residual blurriness, ensuring that important 
details were well-preserved. Overall, the combination of frequency domain processing and 
spatial domain enhancements provided a robust method for image beautification.
Conclusion
This assignment demonstrated the effective use of frequency domain techniques for image 
beautification. By processing each color channel separately and applying a combination of 
FFT, low-pass filtering, bilateral filtering, and brightness adjustments, the images were 
significantly enhanced. The skin appeared smoother and brighter, and the overall visual 
quality was improved.
Future Work
Future improvements could include:
- Adaptive Filtering: Implementing adaptive mask sizes in the frequency domain based on 
image content to better handle varying textures.
- Advanced Smoothing Techniques: Exploring more advanced smoothing techniques to 
further enhance skin texture while preserving natural facial features.
- Machine Learning Integration: Integrating machine learning models to improve skin 
detection and enhancement, allowing for more precise and personalized beautification.
In conclusion, this project successfully applied frequency domain techniques to achieve the 
desired outcome of smoother and brighter skin in the processed images. The methodology 
can be refined and expanded for broader applications in image enhancement and
beautification tasks.
