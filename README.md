# Open-CV-Pyhton
This code is a **comprehensive OpenCV tutorial** covering fundamental image processing techniques. Below is a structured breakdown of the different functionalities implemented:

---

**1. Installing and Importing OpenCV**
- The **OpenCV library** (`opencv-python`) is installed.
- **NumPy** is automatically installed as a dependency.

---

**2. Loading and Converting Images**
- Images are loaded using `cv2.imread()`.
- **BGR to Grayscale conversion** using `cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)`.
- Images are displayed using `cv2.imshow()`, and the window remains open until a key is pressed (`cv2.waitKey(0)`).

---

**3. Color Space Conversion**
- **BGR to HSV** conversion using `cv2.cvtColor(image, cv2.COLOR_BGR2HSV)`.
- This transformation is useful for color-based segmentation and object detection.

---

**4. Drawing Shapes on Images**
- **Line**: `cv2.line(image, start_point, end_point, color, thickness)`
- **Rectangle**: `cv2.rectangle(image, top_left, bottom_right, color, thickness)`
- **Circle**: `cv2.circle(image, center, radius, color, thickness)`
- These functions help in object annotation or graphical overlays.

---

**5. Image Transformations**
(a) **Resizing**
- `cv2.resize(image, (width, height))` adjusts the image size.

(b) **Rotating**
- Uses an **affine transformation** with `cv2.getRotationMatrix2D()` to rotate the image.

(c) **Cropping**
- Extracts a portion of the image using slicing: `image[y1:y2, x1:x2]`.

---

**6. Image Filtering**
(a) **Blurring**
- `cv2.GaussianBlur(image, (11,11), 0)` applies Gaussian blur to remove noise.

(b) **Edge Detection**
- `cv2.Canny(image, 100, 200)` detects edges using the **Canny Edge Detector**.

(c) **Thresholding**
- Converts an image to **binary format** using `cv2.threshold()`, useful for object segmentation.

 (d) **Contours Detection**
- `cv2.findContours()` finds contours in the binary image.
- `cv2.drawContours()` draws detected contours.

---

**7. Face Detection using Haar Cascades**
- Loads a **pre-trained Haar cascade classifier** to detect faces.
- `cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')`
- Draws bounding boxes around detected faces using `cv2.rectangle()`.

---

**8. Video Capture and Processing**
(a) **Capturing Video from Webcam**
- `cv2.VideoCapture(0)` starts webcam feed.
- Frames are continuously captured and displayed in a loop.
- Press **'q'** to exit.

(b) **Saving Video**
- `cv2.VideoWriter()` is used to save frames as a video file (`.avi` format).
- Uses a **fourcc codec** (`XVID`) and writes frames in a loop.

---

**Key Takeaways**
✅ Covers **basic to advanced** OpenCV functionalities.  
✅ Works with **both images and videos**.  
✅ Applies **face detection, edge detection, transformations, and filtering**.  
