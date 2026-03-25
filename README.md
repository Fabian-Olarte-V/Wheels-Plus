# WheelsPlus

WheelsPlus is a native Android application built in Java for coordinating shared rides between drivers and passengers. The project includes authentication, ride group management, real-time location tracking, in-app chat, and route visualization on a map.

## Overview

The app is organized around two main user flows:

- Passenger: search for available ride groups based on origin, destination, and schedule, join a trip, and follow the driver's route in real time.
- Driver: register vehicles, create ride groups, manage passengers, and run the trip from the app.

The application also includes:

- Sign up and sign in with Firebase Authentication
- Optional biometric login
- User, group, chat, and location persistence with Firebase Realtime Database
- Image sharing in chat using Firebase Storage
- Real-time geolocation updates
- Route calculation and drawing using OSMDroid and OSMBonusPack
- Map appearance changes based on the device light sensor

## Main Features

### Passenger flow

- User registration and login
- Current location detection
- Group search by destination, name, and time
- Join available ride groups
- Track the trip and the driver on the map
- Leave a joined group
- Chat with other users

### Driver flow

- Register as a driver during sign up
- Register and manage vehicles
- Create ride groups with origin, destination, fare, schedule, and vehicle
- View passengers assigned to the route
- Follow trip progress on the map
- End trips and remove related trip data
- Chat with passengers

## Tech Stack

- Native Android
- Java
- Gradle
- Firebase Authentication
- Firebase Realtime Database
- Firebase Storage
- Google Play Services Location
- OSMDroid
- OSMBonusPack / OSRM
- Glide
- Lottie
- AndroidX Navigation
- Biometric API

## Requirements

- Android Studio
- JDK 8 or a compatible version for this project
- Android SDK 32
- A physical device or emulator running Android 6.0+
- A valid `google-services.json` file connected to a Firebase project

## Setup

1. Clone the repository.
2. Open the project in Android Studio.
3. Make sure `app/google-services.json` matches your Firebase project.
4. Sync the project with Gradle.
5. Run the app on a device or emulator.

## Permissions

- `ACCESS_FINE_LOCATION`
- `ACCESS_COARSE_LOCATION`
- `INTERNET`
- `ACCESS_NETWORK_STATE`
- `FOREGROUND_SERVICE`
- `RECEIVE_BOOT_COMPLETED`

These permissions are mainly used for maps, real-time location, and startup-related background behavior.

## Project Structure

```text
app/src/main/java/
|- com.example.wheelsplus   -> Main activities and fragments
|- adapters                 -> List and RecyclerView adapters
|- model                    -> Domain models
|- display                  -> UI display models
|- services                 -> Helper services
|- boot                     -> Boot receiver and startup service
```

## Core Models

- `Usuario`: basic user information and current location
- `Vehiculo`: driver vehicle information
- `Grupo`: shared ride group with origin, destination, seats, fare, and schedule
- `Chat`: conversation between two users
- `Mensaje`: text or image messages
- `PuntoRuta`: intermediate route points

## Project Status

This is an older project, so it may require some updates before running smoothly today, especially around:

- Android and Firebase dependency versions
- Firebase configuration
- Compatibility with newer Android versions
- Code cleanup, naming, and UI text consistency

## Possible Improvements

- Upgrade Gradle and library dependencies
- Separate business logic from activities and fragments
- Add meaningful automated tests
- Improve validation and error handling
- Move hardcoded UI strings into `strings.xml`
- Document the Firebase data structure
- Modernize the UI and architecture

## Notes

This repository works well as a portfolio project because it combines Android development, maps, mobility features, real-time data, and messaging in a single app.
