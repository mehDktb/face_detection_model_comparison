# Face Detection Model Comparison

This repository provides a practical evaluation and comparison of popular face detection models under various real-world conditions. The tested models include Haar Cascade, dlib (HOG+SVM and CNN), MTCNN, YOLO variants (v11s and v11n), and RetinaFace.

## Evaluation Conditions

The accuracy and performance of each model were evaluated across diverse scenarios:

* **Angles**: Different facial orientations and positions.
* **Lighting Conditions**: Varied lighting intensities, including bright, medium, and low-light environments.
* **Distances**: Short, medium, and long-range detections.
* **Accessories**: Impact of wearing sunglasses and masks on face detection accuracy.
* **Multiple Faces**: Efficiency in detecting more than one face simultaneously.

## Results Table

| Model         | Speed        | Detection Distance | Angle Stability | Bright Light | Low Light | Mask       | Glasses    | Mask & Glasses | Multiple Faces | Detection Accuracy |
|---------------|--------------|--------------------|-----------------|--------------|-----------|------------|------------|----------------|----------------|--------------------|
| Haar Cascade  | > 30 fps     | ≤ 2 meters         | Very Weak       | Moderate     | Weak      | Weak       | Good       | Very Weak      | Weak           | Weak               |
| dlib-HOG+SVM  | > 30 fps     | ≤ 1 meter          | Weak            | Good         | Weak      | Weak       | Good       | Very Weak      | Weak           | Weak               |
| dlib-CNN      | < 1 fps      | -                  | -               | -            | -         | -          | -          | -              | Very Good      | Very Good          |
| MTCNN         | 5-7 fps      | > 3 meters         | Very Good       | Very Good    | Very Good | Very Good  | Very Good  | Moderate       | Very Good      | Very Good          |
| Yolo v11s     | 10-12 fps    | > 3 meters         | Very Good       | Very Good    | Very Good | Very Good  | Very Good  | Very Good      | Very Good      | Very Good          |
| Yolo v11n     | 15-17 fps    | > 3 meters         | Very Good       | Very Good    | Very Good | Very Good  | Very Good  | Very Good      | Very Good      | Very Good          |
| RetinaFace    | 1 fps        | > 3 meters         | Very Good       | Very Good    | Very Good | Very Good  | Very Good  | Very Good      | Very Good      | Very Good          |

## Recommendations

* **Real-time with multiple people:** YOLO v11n
* **Offline high-accuracy analysis:** RetinaFace
* **Low-resource, fast preview:** Haar Cascade (for basic needs only)
* **Balanced accuracy & speed:** MTCNN / YOLO v11s

## Audience

This resource is particularly valuable for:

* Researchers and students evaluating face detection methods.
* Developers and engineers selecting appropriate models for real-world face detection applications.
* Open-source contributors aiming to enhance model robustness.

## License

This repository is licensed under the MIT License. Feel free to explore, contribute, or utilize the insights provided here to inform your face detection projects.
