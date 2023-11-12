---
title: "What you need to know about React Native"
seoTitle: "React Native: A Comprehensive Guide"
seoDescription: "Discover React Native, explore its applications, and understand its distinctions from React. Uncover the mechanics behind cross-platform mobile development."
datePublished: Sun Nov 12 2023 00:26:27 GMT+0000 (Coordinated Universal Time)
cuid: clouqji4k000108l5hpx065qs
slug: what-you-need-to-know-about-react-native
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699716857893/43bc1d7b-018c-4109-83f8-49c2952d395d.gif
tags: javascript, ios, react-native, android, mobile-development

---

Hello peeps 👋, It's been a while on this platform.

### The story of my life 🫠

Anyway, I am back again to bring us something exciting I have been learning about mobile app development. Earlier this year, I took an interest in learning mobile, which was awkward because I knew nothing about mobile app development and was not sure the programming language I knew would be able to help me. After doing some research and asking some questions, I understood what mobile development was and what the prerequisites were. Also, because I was already a JavaScript developer, I decided to settle for React Native. At first, I wanted to learn something native to Android: Kotlin or Java. Still, achieving all this became longer as I needed to understand the programming languages first before I could start what I wanted.

### Mobile Application Development 📱

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699748138428/47dd6d14-a4f9-409c-8e8c-20e5e58fbfd7.png align="center")

Mobile app development is the process of developing applications that are intended to run on mobile devices, which may include tablets, smart devices, etc. Mobile application development involves a lot of steps, which include design, converting design to codes, testing, deployment, post-maintenance fixes, etc.

### Why do we build mobile apps? 👌👌

Here are some reasons why businesses decide to build mobile apps for their products:

* Improved user experience
    
* Develop a customized marketing challenge
    
* For business growth and increased revenue
    
* Easy accessibility and convenience
    
* For monetization opportunities, e.g. ads, etc
    
* Increased customer experience.
    

### Types of mobile app development 📲📞

1. **Native App Development:** This involves developing apps for a specific OS (either Android or iOS) using codes that these platforms support. For example, Android supports Kotlin and Java programming languages, while iOS supports Swift and Objective-C. Native development is the best form of mobile app development, especially when you're targeting native device features, e.g., cameras, fingerprints, etc. Native development can also provide faster performance.
    
2. **Cross-Platform App Development:** This involves developing applications that can run on multiple OSs with a single code base. This form of development reduces development time as we build simultaneously for multiple OSs. Some popular frameworks that can achieve this are Flutter, Phone Gap, React Native, Xamarin, etc.
    
3. **Progressive Web Apps (PWA):** This involves building apps using web technologies such as HTML, CSS, and JS; hence, they can only be accessed through a web browser and do not need to be downloaded from the App Store or Play Store. To learn more about PWAs, you can check out this [article](https://blog.reactplay.io/building-a-progressive-web-application-pwa-using-react) by @[Franklin Ohaegbulam](@frankiefab100).
    

### What is React Native?🤷🤷🤷🤷🤷🤷

![](https://www.galvanizeaction.org/wp-content/uploads/2022/06/Wow-gif.gif align="center")

Now to the business of the day! What does React Native mean? React Native is a JavaScript framework used to build mobile apps across different platforms, including Android, iOS, web applications, desktop applications, etc. It might interest you that the Facebook team developed React Native primarily to develop mobile apps using JavaScript and React. This means that JavaScript is a must-know before anyone can venture into React Native. It would also be great if you knew React, as it would simplify a lot of concepts.

### Is React Native different from React?

![](https://media.giphy.com/media/gCeh1KDeDaxGu8no4A/giphy.gif align="center")

Yes, of course. First, React was designed for the web, while React Native was designed for building mobile applications. The Facebook team developed both and has the same underlying concept.

> Note: React Native was built on top of React and JavaScript, to enable developers build mobile apps.

React and React Native differ in several ways, which include:

* **Rendering:** React uses the virtual DOM to render web pages in the web browser. While React Native uses JavaScript Core/Hermes Engine, JavaScript threads, and the React Native bridge to render screens on mobile devices,
    
* **Styling:** React uses the default CSS for styling to style HTML elements in the web browser. React Native uses a styling style that is similar to CSS but not CSS.
    

### Why React Native and the Benefits of Using React Native?

React Native is a good framework for building mobile applications. Most products rely on React Native to achieve functionalities. Here are some reasons why React Native is the tool most mobile developers go to for building mobile applications.

Below are some underlying reasons why React Native is React Native is a great choice.

1. **Cross-Platform:** React Native uses a single code base that is valid for both iOS and Android applications. Developers do not need to overwhelm themselves with learning both Swift and Java/Kotlin for the various platforms. React Native abstracts make it easier for developers to complete their tasks on time.
    
2. **Reloading:** Instead of recompiling, you can reload your app instantly. You’re given two options: Live Reloading will reload the app whenever you edit and save one of its files. Hot reloading only reloads the file you just edited, not the entire file.
    
3. **Efficiency:** React Native requires less building time than native app development. Hence, developers can build products in a short period of time.
    

Other benefits of React Native include:

1. Readability
    
2. Declarative-style programming
    
3. Large community base.
    

### How does React Native work?

Hmm, I know this is something that might sound a bit complex, knowing that anyone who reads this is a novice. For posterity's sake, I will be telling us how React Native works, but I will not be going into details in this article, but maybe another.

1. **JavaScript Code:**
    
    React Native applications are primarily written in JavaScript (and JSX). This codebase contains the business logic, component definitions, and other aspects of the application.
    
2. **React Native Bridge:**
    
    The JavaScript code communicates with native modules through the React Native Bridge. The bridge enables the JavaScript runtime to interact with native code in a seamless manner.
    
3. **Native Modules:**
    
    React Native includes a set of core native modules for common functionalities (camera, geolocation, etc.). Additionally, developers can create custom native modules to expose platform-specific features to JavaScript.
    
4. **Platform-Specific Code:**
    
    * React Native applications have folders (`android` and `ios`) containing native code specific to each platform. For example:
        
        * `android`Java and XML files for Android
            
        * `ios`Objective-C or Swift files for iOS.
            
5. **Compilation for Android:**
    
    * For Android, the JavaScript code is bundled and optimized using tools like Metro Bundler. This bundled code is then embedded into the Android project.
        
    * The Android-specific native code is compiled using the Gradle build system. The entire project is built into an Android Application Package (APK) file.
        
6. **Compilation for iOS:**
    
    * For iOS, the JavaScript code is bundled and optimized using tools like Metro Bundler. This bundled code is embedded into the Xcode project.
        
    * The iOS-specific native code is compiled using Xcode. The project is built into an iOS App Bundle (IPA) file.
        
7. **Hermes (Optional):**
    
    * On Android, developers can choose to use the Hermes JavaScript engine for optimized performance. Hermes performs ahead-of-time (AOT) compilation during the build process.
        
8. **Assets and Resources:**
    
    * Images, fonts, and other assets are included in the native projects. These resources are optimized for each platform during the build process.
        
9. **Packaging:**
    
    * The compiled native code bundled JavaScript, and assets are packaged together into the final distribution format:
        
        * Android: APK (Android Application Package).
            
        * iOS: IPA (iOS App Bundle).
            

### Popular apps built with React Native

Some of the popular apps that are built with React Native include

* Instagram
    
* Shopify
    
* Alibaba
    
* Uber Eats
    
* Pinterest
    
* Airbnb
    
* Facebook
    
* Discord etc.
    

### Starting your first React Native app

To get started with your first React Native app, please follow the steps on React [Native's official site](https://reactnative.dev/docs/environment-setup) to install and start your first React Native application.

![](https://i.gifer.com/Fb4B.gif align="center")

To receive an update when the article drops, do well to subscribe to my newsletter or follow me on any of the social media platforms.

Twitter 🐦: @[@nwokporo_ebuka](@nwokporo_ebuka)

LinkedIn ⚡: @[@chukwuebuka_nwokporo](@chukwuebuka_nwokporo)

GitHub 🚀: @[@ebukvick](@ebukvick)

Hashnode 📗: @[Nwokporo Chukwuebuka](@codeDaddy)