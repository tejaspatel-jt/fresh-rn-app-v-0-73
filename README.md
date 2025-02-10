# React Native 0.73.0 Project Setup 🚀

This document provides step-by-step instructions to create, set up, and run a **React Native 0.73.0** project.

---

## 📌 Prerequisites

Before starting, ensure you have the following installed:

- **Node.js**
  - Latest LTS version recommended, I'm using `v18.18.2`
- **npm or yarn**
  - I'm using `9.8.1`
- **Java JDK(for Android development)**
  - I'm using `java 17.0.6`
- **Android Studio (for Android development)**
  - I've installed `Android StudioGiraffe | 2022.3.1`
- **Xcode (for iOS development, Mac only)**
  - I don't have Mac yet `🥲😔😟☹️🥺🥹😥😢😭😖😞😓`.

---

## 🚀 Create a New React Native Project

**1. Run the following command to create a fresh React Native project with version **0.73.0**:**

```bash
npx react-native@0.73.0 init MyNewApp --version 0.73.0
```

**2. After the project is created, open project folder in VS code:**

```bash
cd MyNewApp && code .
```

**3. Check the installed React Native version:**

```bash
react-native --version
```

**4. Start Metro Bundler in 1st Terminal:**

```bash
npx react-native start
```

**5. Run the app on Android/iOS in 2nd Terminal:**

```bash
npx react-native run-android
```

or Run the app on iOS (Mac only):

```bash
cd ios && pod install && cd .. && npx react-native run-ios
```

## 😟 If you face any issues, run:

```bash
rm -rf node_modules package-lock.json android/.gradle android/app/build
npm install
cd android && ./gradlew clean && cd ..
 # On 1st Terminal
npx react-native start --reset-cache
# On 2nd Terminal
npx react-native run-android
```

#### If you get any error related to java JDK version like below

```bash
FAILURE: Build failed with an exception.

* Where:
Build file 'C:\Projects\RN\MyNewApp\android\app\build.gradle' line: 1

* What went wrong:
A problem occurred evaluating project ':app'.
> Failed to apply plugin 'com.android.internal.application'.
   > Android Gradle plugin requires Java 17 to run. You are currently using Java 11.
```

#### Please follow below steps to resolve the JDK Error

Open `gradle.properties` file located at `C:\Projects\RN\MyNewApp\android` add Java 17 path like below at last.( **JDK location can be diff on your machine, so modify accordingly** )

```gradle
org.gradle.java.home=C\:\\setup\\java-17.0.6
```

# ✅ Your fresh React Native 0.73.0 project is ready! 🚀🔥

# ✈️ Sent to github via below bash airlines commands

1. Create repo on `github.com` and then come to the project directory.
2. Hit below commands line by line

```bash
git init
git add .
git commit -m "Initial Very First fucking Fresh commit"
git remote add origin https://github.com/tejaspatel-jt/fresh-rn-app-v-0-73.git
# If you have multiple git accounts on machine Then Only hit below command
git remote set-url origin https://tejaspatel-jt@github.com/tejaspatel-jt/fresh-rn-app-v-0-73.git
# Else this command
git branch -M main
git push -u origin main
```

3. Check your repo on github. It's there now 😎.

## 🚀 Other GIT Commands
1. Remove Untracked Files:

```bash
git clean -fd
```
  - -f: Force the removal of untracked files.
  - -d: Remove untracked directories.

2. Reset Staged Changes:

```bash
git reset HEAD .
```

## 🚀 NPM Commands
### Remove Unused Dependencies
```bash
npx depcheck
```