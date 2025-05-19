# Edge-Detection-Comparison
### Mean Blurring:
### The logic:
The average blur is to reduce the image noise and detail by replacing each pixel value with the average of its neighboring pixels. This is done by applying a kernel (matrix) to each pixel in the image. 
For example, in a 3×3 kernel, the pixel at the center is replaced by the average value of the 9 pixels covered by the kernel. The result is a smoother image with reduced sharpness.
We next demonstrate mean blurring, and to make things interesting, we compare the results when we blur the same image using both the predefined function present in the OpenCV library and the function we built from scratch to demonstrate the concepts. 
### Median Filter: 
### The logic:
Instead of averaging the values of surrounding pixels, it finds the median value from the surrounding pixels and assigns it to the center pixel.
For instance, in a 3×3 window, all 9 pixel values are collected, sorted, and the median (middle) value is used. Since the median is not affected by outliers, this method is better at preserving edges while removing noise.
### Gaussian Blur:
### The logic:
Gaussian blur is a more advanced method that uses a Gaussian function to calculate the weighted average of surrounding pixels. The center pixel has the highest weight, and the influence decreases with distance from the center. This gives a more natural, smooth blur compared to the average method. The Gaussian blur is based on the Gaussian distribution (bell curve), and the kernel values are pre-computed using this formula. The amount of blurring is controlled by the standard deviation (σ). Gaussian blur is very commonly used to reduce noise before applying edge detection because it softens the image while preserving the general structure.
