# healthy-and-junk-food detection on Yolov5 using jetson Nano 2gb

Aim And Objectives :-

Aim :-

Junk food may be quite convenient, readily available on the go, cheap whereas healthy food is best for maintaining weight, getting an adequate amount of essential nutrients and for keeping you in good state of health.

Objectives :-

. The main objective of the project is to create a program which can be either run on Jetson nano or any pc with YOLOv5 installed and start detecting using the camera module on the device.

. Using appropriate datasets for recognizing and interpreting data using machine learning.

. To show on the optical viewfinder of the camera module whether a food belongs to which species.

# Abstract :-

. Eat healthy and live healthy is one of the essential requirements for long life. Unfortunately, todays world has been adapted to a system of consumption of foods which has several adverse effects on health.

. We have completed this project on jetson nano which is a very small computational device.

. A lot of research is being conducted in the field of Computer Vision and Machine Learning (ML), where machines are trained to identify various objects from one another. Machine Learning provides various techniques through which various objects can be detected.

. One such technique is to use YOLOv5 with Roboflow model, which generates a small size trained model and makes ML integration easier.

. The purpose of this project is to observe healthy junk food behaviour.

# Introduction :-
. The junk food contains sugar, salt fats and more which contribute to obesity. Healthy food can help you get rid of all this as it does not contain harmful things. In addition, healthy food also helps you save money. It is much cheaper in comparison to junk food.

. A healthy diet is essential for good health and nutrition. It protects you against many chronic noncommunicable diseases, such as heart disease, diabetes and cancer. Eating a variety of foods and consuming less salt, sugars and saturated and industrially-produced trans-fats, are essential for healthy diet.

. Neural networks and machine learning have been used for these tasks and have obtained good results.

. Machine learning algorithms have proven to be very useful in pattern recognition and classification, and hence can be used for healthy junk food detection as well.

# Jetson Nano Compatibility :-

. The power of modern AI is now available for makers, learners, and embedded developers everywhere.

. NVIDIA® Jetson Nano™ Developer Kit is a small, powerful computer that lets you run multiple neural networks in parallel for applications like image classification, object detection, segmentation, and speech processing. All in an easy-to-use platform that runs in as little as 5 watts.

. Hence due to ease of process as well as reduced cost of implementation we have used Jetson nano for model detection and training.

. NVIDIA JetPack SDK is the most comprehensive solution for building end-to-end accelerated AI applications. All Jetson modules and developer kits are supported by JetPack SDK.

. In our model we have used JetPack version 4.6 which is the latest production release and supports all Jetson modules.


# Proposed System :-
1] Study basics of machine learning and image recognition.
2]Start with implementation
• Front-end development
• Back-end development
3] Testing, analysing and improvising the model. An application using python and Roboflow and its machine learning libraries will be using machine learning to identify whether the cat belongs to which spices.
4] Use datasets to interpret the object and suggest whether the cat on the camera’s viewfinder belongs to which spices.

#Methodology :-
. Healthy food contains good fats and nutrients that are vital for your body. Healthy food items offer your body the strength and the capacity to fight against various diseases. Whereas But junk food is a highly processed food and contains a high amount of calories. These foods are, harmful to your health.

. Eat a lot of vegetables and fruit. Eat a moderate amount of milk, meat, fish, egg and their alternatives (including dry beans) Reduce intake of foods with high fat/oil, salt and sugar content as well as those preserved and processed foods. Drink adequate amount of fluid every day (including water, tea, clear soup, etc) 

. Hence YOLOv5 which is a model library from roboflow for image classification and vision was used.

. There are other models as well but YOLOv5 is smaller and generally easier to use in production. Given it is natively implemented in PyTorch (rather than Darknet), modifying the architecture and exporting and deployment to many environments is straightforward.

. YOLOv5 was used to train and test our model for whether the cat belongs to which species. We trained it for 149 epochs and achieved an accuracy of approximately 92%.

# Installation :-
Initial Configuration :-

sudo apt-get remove --purge libreoffice*

sudo apt-get remove --purge thunderbird*

Create Swap :-

udo fallocate -l 10.0G /swapfile1

sudo chmod 600 /swapfile1

sudo mkswap /swapfile1

sudo vim /etc/fstab

# make entry in fstab file

/swapfile1 swap swap defaults 0 0

Cuda env in bashrc :-

vim ~/.bashrc

#add this lines

export PATH=/usr/local/cuda/bin${PATH:+:${PATH}}

export LD_LIBRARY_PATh=/usr/local/cuda/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

export LD_PRELOAD=/usr/lib/aarch64-linux-gnu/libgomp.so.1

Update & Upgrade :-

sudo apt-get update

sudo apt-get upgrade

Install some required Packages :-

sudo apt install curl

curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py

sudo python3 get-pip.py

sudo apt-get install libopenblas-base libopenmpi-dev

sudo pip3 install pillow

Install Torch :-

curl -LO https://nvidia.box.com/shared/static/p57jwntv436lfrd78inwl7iml6p13fzh.whl

mv p57jwntv436lfrd78inwl7iml6p13fzh.whl torch-1.8.0-cp36-cp36m-linux_aarch64.whl

sudo pip3 install torch-1.8.0-cp36-cp36m-linux_aarch64.whl

# Check Torch, output should be "True"

sudo python3 -c "import torch; print(torch.cuda.is_available())"

Install Torchvision :-

git clone --branch v0.9.1 https://github.com/pytorch/vision torchvision

cd torchvision/

sudo python3 setup.py install

Clone Yolov5 :-

git clone https://github.com/ultralytics/yolov5.git

cd yolov5/

sudo pip3 install numpy==1.19.4

# comment torch,PyYAML and torchvision in requirement.txt

sudo pip3 install --ignore-installed PyYAML>=5.3.1

sudo pip3 install -r requirements.txt

Download weights and Test Yolov5 Installation on USB webcam :-

sudo python3 detect.py

sudo python3 detect.py --weights yolov5s.pt --source 0


# Demo
LINK:- https://youtu.be/_I_Bxqv_Fkg

# Healthy Junk Food Dataset Training :-

# We used Google Colab And Roboflow :-
train your model on colab and download the weights and past them into yolov5 folder link of project colab file given in repo

# Advantages :-
.Why Is Healthy Food Better Than Junk Food? When you consume a diet that is packed with natural fresh produce, it facilitates to lower the risk of several chronic disorders like cancer, obesity, cardiovascular problems, diabetes and many more.
.Healthy food is rich in beneficial nutrients and healthy unsaturated fats.
.Therefore, they help you feel full and energetic throughout the day. In contrast, unhealthy food is high in sodium, sugar, and saturated fats ( bad fats), which can drain your energy levels.
.May help you live longer.
.Keeps skin, teeth, and eyes healthy.
.Supports muscles.
.Boosts immunity.
.Strengthens bones.
.Supports healthy pregnancies and breastfeeding.

# Application :-
.Healthy food is rich in beneficial nutrients and healthy unsaturated fats. Therefore, they help you feel full and energetic throughout the day. In contrast, unhealthy food is high in sodium, sugar, and saturated fats ( bad fats), which can drain your energy levels.

# Conclusion :-
.• In this project our model is trying to detect a cat’s face or body and then showing it on viewfinder, live as whether cat belongs to which species as we have specified in Roboflow.
• The model tries to solve the problem of severe injuries and attack of cats to human that occure in forest and thus protects a person’s life.

# Reference :-
1] Roboflow:- https://roboflow.com/
2] Datasets or images used :- https://www.gettyimages.ae/photos/big-cats?assettype=image&phrase=big%20cats&sort=mostpopular&license=rf%2Crm
3] Google images


