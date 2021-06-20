## Hosted at AWS EC2 
 http://ec2-18-133-180-187.eu-west-2.compute.amazonaws.com:8080/
## Video Recording
  * https://www.loom.com/share/ef295dc856164c658258e475a0f25b0f

# Mammootty Mohanlal Classifier 

## Table of Content
  * [Demo](#demo)
  * [Overview](#overview)
  * [Motivation](#motivation)
  * [Technical Aspect](#technical-aspect)
  * [Installation](#installation)
  * [Run](#run)
  * [Deployement on AWS EC2](#deployement-on-aws)
  * [Directory Tree](#directory-tree)
  * [To Do](#to-do)
  * [Bug / Feature Request](#bug---feature-request)
  * [Technologies Used](#technologies-used)
  * [Team](#team)
  * [License](#license)
  * [Credits](#credits)


## Demo
[![](https://github.com/milangeorge2000/Mammootty_Mohanlal_Classifier/blob/main/static/ee575888-1427-410c-8d68-c41bf58afa86.jpg?raw=true)](https://github.com/milangeorge2000/Mammootty_Mohanlal_Classifier/blob/main/static/d3b760c1-857b-48fa-bf96-f53ef273b9c9.jpg?raw=true)

## Overview
This is a simple image classification Flask app trained which classfies given input into two legendry actors in malayalam "Mammootty and Mohanlal".If an unknown image is given
it gives an output "unknown". It uses MTCNN to detect the faces and InceptionResnetV1(pretrained model) to create the embeddings of faces .

## Motivation
What could be a perfect way to utilize unfortunate lockdown period? Like most of you, I spend my time in learning about machine learning, watching youtube videos, coding and reading some latest research papers on weekends. . I joined a community names Tinkerhub who  community of tinkerers, makers, policy geeks & students and are working towards mapping and empowering people who share a passion to innovate.They recently conducted a program called Build From Home which focuses on building end to end projects. The participants have to choose a stack and have to build an end to end project within 7 days. We have choosen Machine Learning as my stack and choosen the image classification project.

## Technical Aspect
This project is divided into two part:
1. finding out embeddings of faces 
  - Detect Face using MTCNN
  - Create Embeddings using InceptionResnet
  - Store the embeddings along with labels into a file data2.pt
  - Store mtcnn model into data1.pt
  - Store inceptionresnet model into data3.pt
2. Building and hosting a Flask web app on AWS EC2.

## Installation
The Code is written in Python 3.8 If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
pip install -r requirements.txt
```

## Run

To run the app in a local machine, shoot this command in the project directory:
```bash
python app.py
```

## Deployement on AWS EC2
.[[Reference](https://medium.com/techfront/step-by-step-visual-guide-on-deploying-a-flask-application-on-aws-ec2-8e3e8b82c4f7)]

## Directory Tree 
```
├── app 
│   ├── app.py
│   ├── data1.pt
    ├── data2.pt
    ├── data3.pt
│   ├── static
│   └── templates
├── requirements.txt
├── LICENSE
├── Procfile
├── README.md
├── tinkerhub.ipynb
```

## To Do
1. Make the classifier adjust according to variations

## Bug / Feature Request
If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an issue [here](https://github.com/milangeorge2000/tinkerhub/issues/new) by including your search query and the expected result.

If you'd like to request a new function, feel free to do so by opening an issue [here](https://github.com/milangeorge2000/tinkerhub/issues/new). Please include sample queries and their corresponding results.

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://pytorch.org/tutorials/_static/img/thumbnails/cropped/profiler.png" width=200>](https://pytorch.org/) [<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://miro.medium.com/max/750/1*q6F0j8HFHd8jeYXyQBqrCQ.jpeg" width=200>](https://aws.amazon.com/ec2/)

## Team
 Milan Varghese George |
-|
Amal U Nair       |)
## License
[![Apache license](https://img.shields.io/badge/license-apache-blue?style=for-the-badge&logo=appveyor)](http://www.apache.org/licenses/LICENSE-2.0e)

Copyright 2021 Milan Varghese George

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Credits
- My Sincere thanks to Amal U Nair for creating a wonderful UI for this project(www.instagram.com/amalnair9883)
