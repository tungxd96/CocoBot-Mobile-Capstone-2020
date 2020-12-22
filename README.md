# CocoBot-Mobile
CocoBot is an empathetic chatbot application tending to solve caregiver's mental health problems(e.g. depression, asthma, etc.) by:<br/>
- Using conversational AI, Rasa, to understand problems between chatbot and caregivers
- Providing relevant resources to current problems that a caregiver has for contributing to healthcare problem solving
- Tracking current progress of caregiver's solutions to ensure that our caregivers follow their progress properly<br/>
# Getting Started
- [Instructions](#instructions)
  - [Setup](#setup)
    - [Environment Setup](#environment-setup)
    - [Program Setup](#program-setup)
  - [Compile and Run](#compile-and-run)
- [Architecture Diagram](#architecture-diagram)
  - [Fullstack Architecture Diagram](#fullstack-architecture-diagram)
  - [Project Workflow](#project-workflow)
  - [Folder Hierarchy](#folder-hierarchy)
- [Examples](#examples)
  - [Onboarding Questionnaire](#onboarding-questionnaire)
    - [Survey Introduction](#survey-introduction)
    - [Survey Input](#survey-input)
  - [Authentication](#authentication)
    - [Login](#login)
      - [Sign in with Email and Password](#sign-in-with-email-and-password)
      - [Sign in with Apple](#sign-in-with-apple)
    - [Register](#register)
    - [Forgot Your Password](#forgot-your-password)
  - [Settings](#settings)
    - [Personal Information](#personal-information)
    - [Child Information](#child-information)
    - [Notification](#notification)
  - [Progress](#progress)
    - [Progress Stats](#progress-stats)
    - [Progress Details](#progress-details)
- [Demos](#demos)

# Instructions
## Setup
### Environment Setup
- [x] Expo
- [x] Android Studio
- [x] Android Simulator
- [x] IOS Simulator
- [x] Visual Studio Code
### Program Setup
1. On command lines, navigate to where you want to install this program
2. Run `git clone https://github.com/DrDongSi/CocoBot-Mobile.git` to download the program into your current directory
3. Open this project in Visual Studio Code and open a new terminal on VSCode
4. Run `npm install` on terminal to install all required packages and dependencies for the program
## Compile and Run
1. Run `npm start` after completing all the setup
2. Press `i` for IOS stimulator, `a` for Android stimulator, `w` to run on web, or `e` to send a link to your phone with email
# Architecture Diagram
## Fullstack Architecture Diagram
In order to perform CRUD operations from mobile client, it uses [Firebase API](https://docs.expo.io/guides/using-firebase) in [Expo](https://expo.io) to first request HTTP calls to server. From server, it then sends a TCP/IP request to Firebase Authentication and Cloud Firestore for authentication and database communication to the client. <br/>
<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/diagram/architecture-diagram.png">

## Project Workflow
<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/diagram/workflow.png">

## Folder Hierarchy
This folder hierarchy presents all the files that I implemented for this capstone project <br/>
If folder is at the end of its path, that means I implemented all the files inside that folder. If not, my working files will be specified<br/>
<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/diagram/folder-hierarchy.png">

# Examples
## Onboarding Questionnaire
### Survey Introduction
#### Purpose
Introduces to caregivers that we're about to ask caregivers for their information input
#### Steps to Generate Outputs
1. Simply press one of the 2 buttons at the footer of each page to move to the next page

<p float="left">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/1.png" height="450">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/2.png" height="450" hspace="20">
</p>

### Survey Input
#### Purpose
Asks caregivers to input their name, age, household, and children for better assistance and user self-recognition
#### Steps to Generate Outputs
1. Enter name and press `Next`, age input will slide down and be visible for caregivers to enter age and press `Next`
2. Enter household and press next, children input will slide down and be visible for caregivers to enter number of children and press next
3. Press on `+ Add child` to add a child and a modal sheet will appear to allow caregivers entering their child information, then enter their child information per request and press `Save`. After adding a child, any existed children will appear on the screen. Pressing on each child card (e.g. `Cindy` or `Alex`) will allow caregivers to edit their child information. Press `Next` when you're done with children.
4. Press `Explore` to start exploring the app. This will prompt you to our home screen

<p float="left">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/3.png" height="450">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/4.png" height="450" hspace="20">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/5.png" height="450">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/6.png" height="450" hspace="20">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/questionnaire/7.png" height="450">
</p>

## Authentication
To navigate to authentication page, you need to press on the avatar on the header of home screen. This will navigate to settings page. From settings page, if you're signed in, `Log out` button will appear at the bottom of the page. If you're anonymous, `Login` button will appear instead
### Login
#### Purpose
Allows caregivers to login into their own account or sign in with Apple
#### Steps to Generate Outputs
##### Sign in with Email and Password
  1. Enter your email
  2. Enter your password
  3. Press `Sign In`
##### Sign in with Apple
  1. Press `Sign in with Apple` button
  2. Follow Apple sign-in instructions
  
<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/authentication/login.png" height="450">

### Register
#### Purpose
Allows caregivers to create a new account with email and password
#### Steps to Generate Outputs
1. Enter your name
2. Enter your email
3. Enter your password
4. Press `Sign Up`

<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/authentication/register.png" height="450">

### Forgot Your Password
#### Purpose
Allows caregivers to reset their password with Firebase
#### Steps to Generate Outputs
1. Enter your email to send a reset link to your email
2. Press `Submit`, then check your email and follow the instructions in your email to reset your password

<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/authentication/forgot.png" height="450">

## Settings

<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/settings/1.png" height="450">

### Personal Information
#### Purpose
Allows caregivers to view and edit their personal information
#### Steps to Generate Outputs
1. Modify any inputs (first name, last name, gender, date of birth, and email) you want to edit
2. Press `Save` to save any changes
<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/settings/2.png" height="450">

### Child Information
#### Purpose
Allows caregivers to view and edit their children information
#### Steps to Generate Outputs
1. Press on any child card you want to edit his/her information
2. Modify any inputs (first name, last name, gender, date of birth, and chronic condition) you want to edit
3. Press `Save` to save any changes
<p float="left">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/settings/3.png" height="450">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/settings/4.png" height="450" hspace="20">
</p>

### Notification
#### Purpose
Allows caregivers to customize their notification settings
#### Steps to Generate Outputs
1. Press on any switches corresponding to email, daily tasks, messages, and push notifications to toggle on/off a specific notifcation
<img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/settings/5.png" height="450">

## Progress
### Progress Stats
#### Purpose
Provides progress statistics including achievements, ratings in line chart, and solution completion rates in horizontal bar chart
<p float="left">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/progress/1.png" height="450">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/progress/2.png" height="450" hspace="20">
</p>

### Progress Details
#### Purpose
Provides caregivers with progress details including calendar to track their activity period, focus overview, and PST steps
<p float="left">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/progress/3.png" height="450">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/progress/4.png" height="450" hspace="20">
  <img src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/progress/5.png" height="450">
</p>

# Demos
Click on the below thumbnail for video<br/>
<a href="https://youtu.be/a5MP264QC3o">
  <img alt="CocoBot Final Demo" src="https://github.com/tungxd96/CocoBot-Mobile-Capstone-2020/blob/master/images-readme/thumbnail/thumbnail.png" width="400">
</a>
