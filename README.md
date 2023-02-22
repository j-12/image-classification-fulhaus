# image-classification-fulhaus
Image classification model for assessment at Fulhaus

For the dataset, with 100 images of each class -Bed, Chair and Sofa, I developed the following model.

<img width="537" alt="image" src="https://user-images.githubusercontent.com/31993523/220758306-20ba3962-b4f3-4a7e-92a9-ed88d908b3f4.png">

Training data has 240 images and the remaining 60 are used as the validation dataset.

Training and validation accuracy for the model can be seen below as-

<img width="472" alt="image" src="https://user-images.githubusercontent.com/31993523/220758808-8d4a9f61-5542-4684-a242-607256d9f040.png">


After achieving good accuracy, we move on to creating an api to access this model conveniently.

For this purpose, we shall use Flask, and develop a UI too, for a great interactive experience and smooth prediction.

One can clone this repository to run the Flask application 'app.py' and use the service.
For this,
clone this repository using git clone ..
For Mac,
export flask = app.py
flask run

<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

* python 3.8

### Installation


1. Clone the git repository
   ```sh
   git clone https://github.com/j-12/image-classification-fulhaus
   ```
3. Install required packages
   ```sh
   pip install -r requirements.txt
   ```
4. For mac, we assign our app to flask
   ```sh
   export FLASK_APP=app.py 
   ```
5. Run the flask application
   ```sh
   flask run
   ```
6. We get the following output - 
<img width="971" alt="image" src="https://user-images.githubusercontent.com/31993523/220762691-21367d3e-2f9d-4433-8c08-e0a377f68e3e.png">
The app is hosted on localhost, port 5000. You can either click on the link or copy and paste it in a browser of your choice.

We get the following page -

<img width="1107" alt="image" src="https://user-images.githubusercontent.com/31993523/220763487-f8cbb0d6-5bd5-4531-9007-0cb8ccae50a8.png">

We can upload a picture and click on 'Go' to get the classification results-
<img width="1107" alt="image" src="https://user-images.githubusercontent.com/31993523/220764006-02dc601b-4e84-4845-82bb-f7bdb6781bf9.png">

We can see how the model is able to correctly classify the image as a 'Bed' with 99.99% confidence.

<img width="1125" alt="image" src="https://user-images.githubusercontent.com/31993523/220764244-ad34b988-8337-4581-bfdc-e767657e3c45.png">

<!-- Docker Image -->
## Docker Image 

To set up the project easily and to deliver software in ready packages with all the dependencies and their version, we create a Docker image. It consists of everything the software needs to run including libraries, system tools, code, and runtime.

For this, we create a Dockerfile. This text file consists of all the commands a user could call on the command link to assemble an image. Please refer to 'Dockerfile' to check it out. //add link

Next, we build a requirements.txt that has all the information about libraries and their versions that would be required for our project. //add link
   ```sh
   pip freeze > requirements.txt
   ```
We also need to install Docker dektop, it can be easily done by going to docker and installing the relevant one-
(https://www.docker.com)

Next, we build an image -
   For Windows
   ```sh
   docker build --tag [NAME] .
   ```
   For Mac/Linux
   ```sh
    docker build --platform=linux/arm64 --tag [NAME] .
   ```
We can check if the image is exported by
   ```sh
   docker images
   ```
We can also check out the image in Docker Desktop app.

We can now run the image by -
  Windows-
   ```sh
   docker run --name [Container_Name] [Tag given to the image] 
   ```
   
  Mac/Linux
   ```sh
   docker run --platform=linux/arm64 --name [Container_Name] [Tag given to the image] 
   ```






<p align="right">(<a href="#readme-top">back to top</a>)</p>

