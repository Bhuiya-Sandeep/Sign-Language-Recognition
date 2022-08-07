# Sign Language Recognition

Sign language recognition is a problem that has been addressed in research for years. However, we are still far from finding a complete solution available in our society.

Among the works developed to address this problem, the majority of them have been based on basically two approaches: contact-based systems, such as sensor gloves; or vision-based systems, using only cameras. The latter is way cheaper and the boom of deep learning makes it more appealing.

## Vision System
Vision is a key factor in sign language, and every sign language is intended to be understood by one person located in front of the other, from this perspective, a gesture can be completely observable. Viewing a gesture from another perspective makes it difficult or almost impossible to be understood since every finger position and movement will not be observable.

Trying to understand sign language from a first-vision perspective has the same limitations, some gestures will end up looking the same way. But, this ambiguity can be solved by locating more cameras in different positions. In this way, what a camera can’t see, can be perfectly observable by another camera.

The vision system is composed of two cameras: a head-mounted camera and a chest-mounted camera. With these two cameras we obtain two different views of a sign, a top-view, and a bottom-view, that works together to identify signs.

![This is an image](https://miro.medium.com/max/972/1*Xa4eHvpAkQWh627Y15CsQA.png)
## DATASET
To develop the first prototype of this system is was used a dataset of 24 static signs from the Panamanian Manual Alphabet.

![This is an image](https://miro.medium.com/max/1050/1*qENlFlODgFtb1QzFXqfE_w.png)
To model this problem as an image recognition problem, dynamic gestures such as letter J, Z, RR, and Ñ were discarded because of the extra complexity they add to the solution.

## Data augmentation
Since the preprocessing before going to the convolutional neural networks was simplified to just rescaling, the background will always get passed to the model. In this case, the model needs to be able to recognize a sign despite the different backgrounds it can have.

To improve the generalization capability of the model it was artificially added more images with different backgrounds replacing the green backgrounds. This way it is obtained more data without investing too much time.


During the training, it was also added another data augmentation process consisting of performing some transformations, such as some rotations, changes in light intensity, and rescaling.
## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install Sign Language Recognition
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
