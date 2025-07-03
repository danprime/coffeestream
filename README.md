This complete webpage provides a fully functional coffee pourover stream detector using OpenCV.js. Here's what it includes:

Key Features:
-------------

1.  **Camera Access**: Uses getUserMedia() to access the phone's back camera

2.  **ROI Calibration**: Click "Calibrate ROI" then tap on the video where the coffee stream appears

3.  **Real-time Detection**: Uses OpenCV.js for robust computer vision processing

4.  **State Classification**: Detects STREAMING, DRIPPING, STOPPED, and NO\_DETECTION states

5.  **Visual Feedback**: Real-time status display with motion levels and stream count

6.  **Detection History**: Logs all state changes with timestamps

7.  **Mobile-Optimized**: Responsive design that works well on phones


How It Works:
-------------

### Computer Vision Pipeline:

*   **Grayscale Conversion**: Reduces computational load

*   **Automatic Thresholding**: Handles varying lighting conditions

*   **Contour Detection**: Identifies shapes in the image

*   **Shape Analysis**: Classifies contours by area and aspect ratio

*   **Motion Detection**: Tracks total pixel changes between frames


### State Classification Logic:

*   **STREAMING**: Large contours with high aspect ratio (tall/thin)

*   **DRIPPING**: Smaller, more circular contours

*   **STOPPED**: No significant motion detected for 1+ seconds

*   **NO\_DETECTION**: No contours found above threshold


### Performance Optimizations:

*   **ROI Processing**: Only analyzes the specified region

*   **Efficient Memory Management**: Properly deletes OpenCV matrices

*   **Frame Rate Management**: Uses requestAnimationFrame for smooth performance


Usage Instructions:
-------------------

1.  **Setup**: Position your phone to view the pourover area

2.  **Calibrate**: Click "Calibrate ROI" and tap where the coffee stream appears

3.  **Start**: Click "Start Detection" to begin monitoring

4.  **Monitor**: Watch the real-time status updates

5.  **Complete**: Get notified when the pour stops


The app will automatically detect when the coffee stream transitions from a steady pour to drops and finally stops completely. It's designed to be robust against lighting changes and coffee stream variations while providing clear visual feedback throughout the process.
