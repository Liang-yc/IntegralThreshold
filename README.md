# IntegralThreshold
Adaptive Thresholding Using the Integral Image.

Based on https://github.com/phryniszak/AdaptiveIntegralThresholding Converted to Python.
For more details, please read this papaer [Adaptive Thresholding Using the Integral Image](https://www.researchgate.net/publication/220494200_Adaptive_Thresholding_using_the_Integral_Image).

This method can preserve more image details as the table shows.  
<table>
<thead><tr><th>image</th><th>OTSU thresholding</th></tr></thead>
        <tr>
            <td><a href=""><img width="100%" style="max-width: 30%;max-height:30%;" alt="" src="https://github.com/Liang-yc/images4readme/blob/master/red_plate.JPG" ></a></td>
            <td><a href=""><img width="100%" style="max-width: 30%;max-height:30%;" alt="" src="https://github.com/Liang-yc/IntegralThreshold/blob/master/otsu_results.jpg" ></a></td>
        </tr>
  <tr><th>image</th><th>OTSU thresholding</th></tr></thead>
        <tr>
            <td><a href=""><img width="100%" style="max-width: 30%;max-height:30%;" alt="" src="https://github.com/Liang-yc/images4readme/blob/master/red_plate.JPG" ></a></td>
            <td><a href=""><img width="100%" style="max-width: 30%;max-height:30%;" alt="" src="https://github.com/Liang-yc/IntegralThreshold/blob/master/otsu_results.jpg" ></a></td>
        </tr>
</table>

The code is simple but the speed is insanely slow when the image is very large; and I use [numba](http://numba.pydata.org/) to speed up. The original code consumes more than 3 minutes for processing this test immage while it only costs about 1 seconds with numba.
