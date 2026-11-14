> **Previous implementation — see the current MQTT Fundamentals example.** This repository is preserved as a reference for the original Swing/Blackboard design. For the actively maintained Java MQTT tutorial and a simpler Brokerverse GUI that share `Parcel`, `Publisher`, and `Subscriber`, visit **[MQTT Fundamentals](https://github.com/csc-3100/cloud-mqtt-fundamentals)**. This repository is no longer the recommended starting point.

![Static Badge](https://img.shields.io/badge/author-javiergs-orange)
![GitHub repo size](https://img.shields.io/github/repo-size/javiergs/App-MQworld)
![Java](https://img.shields.io/badge/Java-17+-blue)
![Platform](https://img.shields.io/badge/platform-Java_Swing-orange)

<p align="left">
  <img width="100" alt="MQWorld Logo" src="https://github.com/user-attachments/assets/9daa43d3-9c49-4271-8f12-72e9d1bf631b" />
</p>

A simple Java Swing application where multiple instances connect to a shared virtual grid and publish or receive each other’s positions in real time via MQTT.
It demonstrates the **publish–subscribe pattern** using the Eclipse Paho MQTT client library and a public MQTT broker.  

MQWorld is an **experimentation sandbox**:
- Change the topic structure  
- Swap the broker  
- Adjust the visuals  
- Scale the world  
- Extend the logic with new agents or interactions  

## 🚀 Features

-   MQTT publish--subscribe architecture using Paho.
-   Real‑time synchronization of multiple clients in the same shared "world".
-   Lightweight Java Swing GUI.
-   Thread‑safe "Blackboard" shared‑memory model separating model, view, and controller.
-   Automatic reconnection and MQTT session management.
-   Easily extensible.

## 🛠 Run the application

    java -jar target/MQWorld-1.0.jar player1
    java -jar target/MQWorld-1.0.jar player2

## 🕹️ Controls

| Key | Action     |
|-----|------------|
| ↑   | Move Up    |
| ↓   | Move Down  |
| ←   | Move Left  |
| →   | Move Right |

## 📁 Project Structure

-   Main.java -- entry point
-   Blackboard.java -- shared model
-   WorldPanel.java -- renderer
-   Player.java -- player model
-   Publisher.java -- MQTT publisher
-   Subscriber.java -- MQTT subscriber
