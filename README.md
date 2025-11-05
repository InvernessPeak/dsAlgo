# dsAlgo Connects: Your Private, Real-Time Communication Hub

**dsAlgo Connects is a full-featured, real-time chat and video calling web application built with a strong focus on user privacy and anonymity.**

Unlike mainstream apps that require personal phone numbers, dsAlgo Connects uses a unique, shareable ID system (`jg-xxxx`), allowing you to connect and communicate securely without revealing your real-world identity. This project is built entirely with vanilla JavaScript, Firebase, and WebRTC, demonstrating a powerful, serverless architecture.


---

## ✨ Core Features

-   **Real-Time Anonymous Chat:** Secure 1-on-1 messaging with a unique ID system. No phone numbers required.
-   **Advanced Messaging:** Includes a three-stage message status system: ✅ Sent, ✅✅ Delivered, and ✅✅ Seen (Blue Ticks).
-   **HD Voice & Video Calls:** Crystal-clear, peer-to-peer calls powered by WebRTC.
-   **Rich Presence System:** See when your friends are `🟢 Online` or `⚫ Offline` in real-time.
-   **Full Profile Customization:** Set your display name, a representative emoji, and upload a custom profile picture.
-   **Modern UI/UX:**
    -   Beautiful Day ☀️ and Night 🌙 modes with a stylish animated toggle.
    -   Stunning, gradient-based chat backgrounds.
    -   Intuitive search functionality for chats and calls.
    -   Interactive splash screen for a smooth app launch.
    -   Mobile-first design with support for system back buttons.
    -   Double-tap any non-functional area to instantly hard-reload the app.
-   **Friend Management System:** Send, accept, or reject friend requests, and manage your contacts.
-   **Privacy Controls:** Block and unblock users at any time.

---

## 🛡️ A Focus on Privacy

In a world where every application demands your personal information, dsAlgo Connects offers a refreshing alternative. The core philosophy is to provide a secure and feature-rich communication tool without compromising your anonymity.

-   **No Phone Numbers:** Your account is tied to your email for password recovery, but your identity to other users is your unique **dsAlgo ID** (`jg-xxxx`).
-   **You Control Your Connections:** You can only be contacted by users with whom you have explicitly shared your ID and accepted a friend request.
-   **Client-Side Logic:** The app runs entirely in your browser, with all data managed securely through your personal Firebase instance.

---

## 🚀 Live Demo & Installation

### Live Demo

You can try a live version of the app here: **[dsAlgo Live Demo](https://invernesspeak.github.io/dsAlgo_Connects/)**

### Local Installation & Setup

To run this project locally, you will need to set up your own Firebase backend.

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/InvernessPeak/dsAlgo.git
    cd dsalgo
    ```

2.  **Set up Firebase**
    -   Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
    -   In your new project, enable **Authentication** -> **Sign-in method** -> **Email/Password**.
    -   In the sidebar, go to **Realtime Database** and create a new database. Start in **test mode** for now.
    -   Go to your **Project Settings** (click the gear icon ⚙️). Under the "General" tab, scroll down to "Your apps".
    -   Click the web icon (`</>`) to register a new web app.
    -   After registering, Firebase will give you a `firebaseConfig` object. Copy this object.

3.  **Configure the App**
    -   Open the `index.html` file (or whatever you have named your main HTML file).
    -   Find the `<script>` tag at the bottom and locate the `firebaseConfig` object.
    -   **Replace the placeholder object** with the one you copied from your Firebase project.

    ```javascript
    // --- FIREBASE CONFIG ---
    const firebaseConfig = {
        apiKey: "YOUR_API_KEY",
        authDomain: "YOUR_AUTH_DOMAIN",
        databaseURL: "YOUR_DATABASE_URL",
        projectId: "YOUR_PROJECT_ID",
        storageBucket: "YOUR_STORAGE_BUCKET",
        messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
        appId: "YOUR_APP_ID"
    };
    ```

4.  **Run the Application**
    -   This app requires a **secure context** (`https-` or `localhost`) for the camera and microphone permissions to work.
    -   The easiest way to run it is with the **Live Server** extension in Visual Studio Code.
    -   Right-click the `index.html` file and select **"Open with Live Server"**.

---

## How to Use dsAlgo

1.  **Sign Up:** Create a new account using your email and a password.
2.  **Set Up Your Profile:** You will be prompted to create your initial profile with a name and an emoji.
3.  **Find Your ID:** Click the profile icon in the top right to open your profile modal. Your unique `jg-xxxx` ID will be displayed.
4.  **Share & Add Friends:** Share your ID with a friend. To add them, click the "Add Friend" icon and enter their ID.
5.  **Communicate:** Once they accept your request, they will appear in your chats list. Tap on their name to start messaging, voice calling, or video calling!

The Final one: 
you can install and use the mobile application as well from here : https://github.com/InvernessPeak/dsAlgo/blob/main/dsAlgo.apk

