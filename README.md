# WellnessQ

[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![Slack](https://img.shields.io/badge/Join-Slack-blue)](https://callforcode.org/slack) [![Website](https://img.shields.io/badge/View-Website-blue)](https://code-and-response.github.io/Project-Sample/)

Automation tool that virtualizes the waiting Queue At medical centers, Labs and  hospital. Specifically during the hour of crisis like Covid-19 pandemic.


*Read this in other languages: [English](README.md), [한국어](README.ko.md), [português](README.pt_br.md).*

## Contents

1. [About Existing Medical Procedure](#About-Existing-Medical-Procedure)
1. [Demo video](#demo-video)
1. [The architecture](#the-architecture)
1. [Long description](#long-description)
1. [Project roadmap](#project-roadmap)
1. [Getting started](#getting-started)
1. [Running the tests](#running-the-tests)
1. [Live demo](#live-demo)
1. [Built with](#built-with)
1. [Contributing](#contributing)
1. [Versioning](#versioning)
1. [Authors](#authors)
1. [License](#license)
1. [Acknowledgments](#acknowledgments)

## About Existing Medical Procedure

The existing PCR test is registered through a self reporting form for COVID-19 Sample collection.
After submission of the form the mobile number provided in the form gets the OTP , id, Sample ID as a text message. 
They also get provided a link to download ICMR Specimen Referral Form For Covid-19(SARS-CoV2).At Medical centers and collection centers they do not have the real-time tracking application for queue status while waiting at the quarantined place for their turn to appear.

### Problem Statement

The Medical centers and collection centers do not have the real-time tracking application for queue status while waiting at the quarantined place for their turn to appear.

### How can technology help?

We can automate the queue into virtual one so that the patient does not have to stay anxious for its turn for long. It can track the people those are there before and stay alert about its turn. we as well as send the certificate of people who tested negative. Apart from the Covid-19 patients, it can also help the other category of health  department. which will facilitate patients to stay safe while maintaining safe social distancing

### The Idea: Solution

 1. Multiple categories: one category will be covid-19 
 2. Inside that the user has to answer certain questions 
 3. Recommend the user with the list of test/Health facility centers nearer
 4. Option to select an appointment slot time
 5. In that slot, option to view number of people in Queue                
 6. Request for queue Token 
 7. Option track users turn 
 8. Responsive notification alert 
 9. Downloading certificate for Tested negative reports 


## Demo video

[![Watch the video](https://github.com/Code-and-Response/Liquid-Prep/blob/master/images/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)

## The architecture

![Video transcription/translation app](https://developer.ibm.com/developer/tutorials/cfc-starter-kit-speech-to-text-app-example/images/cfc-covid19-remote-education-diagram-2.png)

1. Login 

    a. Generate OTP
    b. Login using OTP
    c. Select type 
         c1. Doctor
         c2. Patient
    d. Edit profile
    e. View Notification
    f. Logout


2. Search/Select for available 
     
     a. View All Health Category
     b. Search available doctors, health center and labs for a perticular slot and department
     c. View My requests for queue
     d. View number of appointments already taken for a particular time slot

3. Request and track
    
      a. Request for Queue
      b. Delete your request
      c. Get real-time notification when queues are updated 

4. The android app uses push notification service and gcm service

5. The android app makes REST API calls to spring boot backend to get records of users

6. The Spring boot backend is connected to MongoDB in cloud

7. The Software product WellnessQ is deployed in IBM cloud foundry Application
 



## Long description

[More detail is available here](DESCRIPTION.md)

## Project roadmap

![Roadmap](roadmap.jpg)

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```bash
Install Java Eclipse
Install Android Studio
Create mongoDB account
Create IBM cloud foundry Application
Create IBM cloud push notification service

bash install.sh
```

### Installing



1. Spring-boot backend set up

```bash
import existing maven project
maven install
maven build and set goal to "spring-boot:run"
Application is now running on tomcat server
Server running at http://localhost:8080/
```

2. Android Native Set up

```bash
curl localhost:3000
Thanks for looking at Code-and-Response!
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why, if you were using something like `mocha` for instnance

```bash
npm install mocha --save-dev
vi test/test.js
./node_modules/mocha/bin/mocha
```

### And coding style tests

Explain what these tests test and why, if you chose `eslint` for example

```bash
npm install eslint --save-dev
npx eslint --init
npx eslint sample-file.js
```

## Live demo

You can find a running system to test at [wellnessq.mybluemix.net](http://callforcode.mybluemix.net/)

## Built with

* [IBM Cloudant](https://cloud.ibm.com/catalog?search=cloudant#search_results) - The NoSQL database used
* [IBM Cloud Functions](https://cloud.ibm.com/catalog?search=cloud%20functions#search_results) - The compute platform for handing logic
* [IBM API Connect](https://cloud.ibm.com/catalog?search=api%20connect#search_results) - The web framework used
* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/Code-and-Response/Project-Sample/graphs/contributors) who participated in this project.

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Based on [Billie Thompson's README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).
