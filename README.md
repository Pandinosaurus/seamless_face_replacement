# Automatic Seamless Face Replacement in Videos
-Yiren Lu (luyiren [at] seas [dot] upenn [dot] edu)
-Dongni Wang (wdongni [at] seas [dot] upenn [dot] edu)

## Project Description
<https://github.com/stormmax/seamless_face_replacement/blob/master/project_description.pdf>




## Run Code

Python third party libs required:
  - dlib
  - cv2
  - skimage
  - scipy.io

To run face replacement:
- Download face landmark estimation model and uncompress
```
$ wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
$ tar xvfj shape_predictor_68_face_landmarks.dat.bz2
```
- Face detection (for both source video and destination video)
```
$ Python face_detect_wrapper.py shape_predictor_68_face_landmarks.dat [video_name_no_suffix]
```
e.g.:
```
$ Python face_detect_wrapper.py shape_predictor_68_face_landmarks.dat clips/clip1
```
Example outputs in `Proj4_Test/` and `clips/`

- Face replacement: see `demo.m`
  - load face detection results output by 1.
  - run replace_all_faces([src video path], [replacement video path], [src video detection results], [source video detection results], [destination video detection results], [source face index], [resize x])
  - save video to .avi file

Example output videos in `output_videos/`

## Video Demo
[![Face replacement](video_screenshot.png)](https://www.youtube.com/watch?v=nZL8UIkghto&feature=youtu.be "Face replacement")

