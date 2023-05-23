# Basic_ANPR_Model

In this model, you can conveniently upload an image of a vehicle to extract its number plate information.

The fundamental model presented here is designed to recognize and extract number plates from vehicle images. The approach to this project involves several logical steps. Initially, the user uploads an image of the vehicle containing the desired number plate, followed by applying grayscale conversion to the image.

Subsequently, a series of intuitive procedures are employed. These include noise cancellation and edge detection using the cv2.bilateralFilter() and cv2.Canny() functions, respectively. Contour detection is then utilized, wherein ten contours are selected and sorted in descending order.

Further filtering is applied to identify contours consisting of exactly four points, as number plates typically possess a rectangular shape defined by four corners. The contour coordinates are extracted and employed to create a mask using numpy and cv2 techniques.

The final step involves reading the text from the number plate. To facilitate this process, the number plate is first cropped to isolate it. Then, by utilizing the easyocr library, the text on the number plate is extracted, yielding the desired outcome along with a confidence measure.

Please note that in some cases, this method may yield inaccurate results if the image contains excessive clutter or if the text on the number plate is unclear.
