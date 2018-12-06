# The Last Post Thermal Dataset

Authors: Jerico Moeyersons & Brecht Verhoeve

Camera operator: Brecht Verhoeve

Camera: FLIR One Pro (Android)

Download Link: [https://cloud.ilabt.imec.be/index.php/s/TNQBfwQkpnRa7Dq](https://cloud.ilabt.imec.be/index.php/s/TNQBfwQkpnRa7Dq)

## About this Dataset

This dataset contains thermal videos of the Last Post ceremony at Ypres. The videos show the arrival of people at the event,
their behaviour during the event and their departure. Sometimes special events, such as a Hakka, army marching or heavy rain
can be seen.

It also contains some ready-to-use images for training with YOLO.

## Video Creation

Videos were made with the Flir One Pro Android USB-C device using a Samsung Galaxy S8. The videos are contained in mp4 files.

## Structure of the Dataset

In the folder 'last_post' all videos can be found. The videos are ordered per date that they were filmed. The dataset are: 24/03/18, 02/04/18, 03/04/18, 04/04/18, 05/04/18, 09/04/18, 10/04/18, 11/04/18 and 12/04/18. In each folder containing a date three subfolders and an info.txt file can be found. The info.txt file contains a description of the conditions the day the videos were made, for each video the duration, what can be seen in the video, the thermal colorscheme used and optional annotated images which explain objects in each scene. In the videos folder the original videos (raw data) can be found. In the annotated images folder optional annotated images per video can be found. The images folder is empty, but can be used as output folder for image extraction from the videos (see Image Extraction section).

In the folder 'yolo_dataset' some images with annotations can be found. These images are ready to use for training and testing in the YOLO real-time object detection system ([https://pjreddie.com/darknet/yolo/](https://pjreddie.com/darknet/yolo/)).

## Image Extraction

In the root directory, a Python script called `image_extraction.py` can be found. This script extracts the individual frames from each video from the videos folders and places them in the images folders. The created images are saved using the JPEG encoding. These images can then be used for learning algorithms. The script requires a working installation of the program 'ffmpeg' and the Python library 'ffmpy'. 'ffmpeg' can be installed with your favourite package manager. To install ffmpy execute: `pip install ffmpy`

Note: this script only works with Python 3.0 or higher.

## Screens

![Thermal Image](https://github.com/IBCNServices/Last_Post_Dataset/blob/master/screens/2018-04-05_20.18.38-01.png "")

![Thermal Image](https://github.com/IBCNServices/Last_Post_Dataset/blob/master/screens/2018-04-10_22.27.23.jpg "")

![Thermal Image](https://github.com/IBCNServices/Last_Post_Dataset/blob/master/screens/flir_20180405T202518.jpg "")

## Disclaimer

The Last Post Dataset is developed at [Ghent University](https://www.ugent.be/en) - [IDLab](https://www.ugent.be/ea/idlab/en) and [imec](https://www.imec-int.com). 
We strongly encourage fellow researchers within the field to try out and use the dataset for their own research projects. 
If you use this dataset for your own projects, please give credit to the original authors, for example by citing the following publication:

> Jerico Moeyersons, Brecht Verhoeve, Pieter-Jan Maenhaut, Bruno Volckaert & Filip De Turck. Pluggable Drone Imaging Analysis Framework for Mob Detection duringOpen-Air Events. (TO BE COMPLETED!) 2019.

<!---## License

Copyright 2018-2019 Ghent University - imec - IDLab

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.-->