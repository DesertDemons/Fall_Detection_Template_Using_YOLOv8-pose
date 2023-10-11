# Fall_Detection_Template_Using_YOLOv8-pose
YOLO Pose Detection for Fall Detection: A Python-based solution to detect fallen persons using YOLO pose estimation.

# YOLO Pose Detection for Fall Detection

A Python-based solution that employs YOLO pose estimation to detect fallen persons in images and videos, complete with a control panel for user input.

## Overview

This research project aims to detect fallen persons in images and videos using the YOLO pose estimation model. The approach is iterative, with each iteration refining the detection mechanism based on the insights from the previous steps.

## Prerequisites

- Python 3.x
- OpenCV
- ultralytics YOLO
- cvzone
- Google Colab (if running in Colab environment)

## Control Panel

The system is equipped with a control panel that allows users to:
- Choose the video file path for video-based detection.
- Specify the image directory for image-based detection.

## Approach and Iterations

1. **Video Detection**: 
   - The initial approach focused on detecting fallen persons in videos. The logic was based on the proximity of the head and hips in the vertical axis.

2. **Single Image Detection**: 
   - The approach was then extended to detect fallen persons in individual images.

3. **Set of Images with YOLOv8n-pose**: 
   - The third iteration processed a set of images using the YOLOv8n-pose model. This model provided keypoint estimation, which was crucial for determining the posture of the detected persons.

4. **Accuracy Enhancement with YOLOv8x-pose-p6**: 
   - To improve the accuracy of the detection, a larger YOLO model, YOLOv8x-pose-p6, was employed. This model provided a more detailed pose estimation, enhancing the reliability of the detection mechanism.

5. **Horizontal Proximity Check**: 
   - The final iteration added a horizontal check to the logic. This check determined if the head and hip were close to each other in the horizontal axis, providing an additional criterion to ascertain if a person has fallen.

## Logic Behind Fall Detection

The foundational logic for detecting a fallen person is predicated on the spatial relationship between the head and hips. If these keypoints are in close proximity, either vertically or horizontally, it is indicative of a fallen posture. While this heuristic is effective in many scenarios, it may require further refinement for edge cases, such as sitting postures.

## Contributing

Researchers and developers are encouraged to contribute to this project. For significant modifications or enhancements, kindly open an issue first to discuss the proposed changes.

## License

[MIT](https://choosealicense.com/licenses/mit/)

