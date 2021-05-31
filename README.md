# LambChat Application

[Live Site](https://lambchat.netlify.app/)

[![React-Firebase-Chat-App-Sign-In.png](https://i.postimg.cc/44DmPbt8/React-Firebase-Chat-App-Sign-In.png)](https://postimg.cc/yWT1YRL9)
[![LambChat.png](https://i.postimg.cc/wxmB1yPD/LambChat.png)](https://postimg.cc/QVjDPtjM)

## Introduction
This is an application developed primarily to utilize Firebase authentication. After signing in using Google or Facebook, the user is prompted to create a chat with other users. This was created using React-Chat-Engine.

### Setup
- Create .env file in the root directory
```
REACT_APP_CHAT_ENGINE_KEY=(YOUR_CHAT_ENGINE_KEY)
REACT_APP_CHAT_ENGINE_ID=(YOUR_CHAT_ENGINE_ID)
```
- Navigate to /src and create a firebase.js file
```js
import firebase from 'firebase/app'
import 'firebase/auth'

/* 
   This can be more easily obtained by creating a project in Firebase, then navigating to the project settings
   From there, in 'general' scroll down until you see SDK setup and configuration
   Select 'Config' and copy/paste the code given
*/

export const auth = firebase.initializeApp({
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGE_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
}).auth()
```
