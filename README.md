# Similarity-Checker
**Tools and Technologies used are docker,docker-compose,MongoDB,Flask,Postman**(to test the API).

Similarity-Checker is a RESTful API made using an NLP model.
This API is made in **flask** using docker-compose as tool to provide end to end user experience without any hassle and easily producible on any server.
The Objective of this API is to simulate the day to day use cases along with some flavor of text similarity checking.

  - Allows user to **Register** and provide them 3 tokens initially to use the service for free
  - Concept of **Hashing** is used to store user password
  - Database used is **MongoDB**
  - A NLP model called **spacy** is used to detect the similarity of the text which is calculated in ratio between 0 and 1
  - Networking concept is used

# Features

  - After consumption of all the tokens, user after knowing the admin password can refill the token and start using the service again.
  - Restricted the same user to enter again and taken care of all the corner cases like invalid username, password combination and all other errors such that other user could not exploit it.
  - Docker is used to provide OS level virtualization.

  ![Screenshot (888)](https://user-images.githubusercontent.com/78041915/107001446-a3cd2380-67af-11eb-9a8a-0b0683caba7c.png)
![Screenshot (889)](https://user-images.githubusercontent.com/78041915/107001598-eb53af80-67af-11eb-9239-23df7d2d3f4f.png)
![Screenshot (890)](https://user-images.githubusercontent.com/78041915/107001601-ed1d7300-67af-11eb-97e9-fe1fae883d63.png)
![Screenshot (891)](https://user-images.githubusercontent.com/78041915/107001602-ed1d7300-67af-11eb-9069-55c204c8e545.png)
![Screenshot (892)](https://user-images.githubusercontent.com/78041915/107001603-edb60980-67af-11eb-8798-15107225bfbe.png)
![Screenshot (893)](https://user-images.githubusercontent.com/78041915/107001605-ee4ea000-67af-11eb-9704-240185e7bbfc.png)
![Screenshot (894)](https://user-images.githubusercontent.com/78041915/107001607-eee73680-67af-11eb-9a71-f2e62bbbffa1.png)


## There is only one branch in this repository i.e `master`  branch

### For `master` branch
* For Flask 1+
* Works with Python 3.9+
* `Dockerfile` for connecting to Docker Hub

```
The template structure is as follows:
├── db
│   └── Dockerfile        <- for connecting to database MongoDB using dockerhub
├── docker-compose.yml    <- to control all the communications i.e basically contains all the containers
├── README.md
└── web
    ├── app.py            <- contains all the apps for the project. New apps should be added to this particular package only.
    ├── Dockerfile        <- docker expects to see a file called dockerfile to run the virtualization
    ├── en_core_web_sm-2.2.0.tar.gz   <- offline model
    └── requirements.txt  <- include dependencies to run the app
```

# How to Install and run
Prerequisites
`Docker`,`Docker-Compose` and `MongoDB` must be installed on your system.

If not installed instructions can be found here:
#### To Install docker and docker-compose
To install `docker` head over [here](https://docs.docker.com/engine/install/ubuntu/) and `docker-compose` [here](https://docs.docker.com/compose/install/)

#### To Install MongoDB
To install `MongoDB` head over [here](https://websiteforstudents.com/how-to-install-mongodb-on-ubuntu-20-04-18-04/)

### To run locally
```
$ mkdir my_project
  --template=https://github.com/harsh-hustler/Similarity-Checker/archive/master.zip
  --extension=py
$ sudo apt install python3-pip
$ pip3 install flask
$ pip3 install bcrypt
$ python -m spacy download en_core_web_sm
$ sudo docker-compose build
$ sudo docker-compose up
$ postman .
```
