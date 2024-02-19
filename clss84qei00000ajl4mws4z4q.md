---
title: "Enhancing Your React Native App: A Guide to Custom Fonts"
seoTitle: "Ultimate Guide to Custom Fonts: Elevate Your React Native App"
seoDescription: "Learn how to enhance your React Native app with custom fonts. Elevate your design and improve user experience with this comprehensive guide."
datePublished: Mon Feb 19 2024 00:54:22 GMT+0000 (Coordinated Universal Time)
cuid: clss84qei00000ajl4mws4z4q
slug: enhancing-your-react-native-app-a-guide-to-custom-fonts
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708299590707/e7577193-a075-45ed-8ef3-c4964320d420.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1708303783817/a641c38f-e548-4c1e-bdfa-73971630c79c.png
tags: react-native, mobile-app-development, mobile-development, custom-fonts, custom-fonts-in-react-native

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708303548181/db809b4b-464c-4449-9d19-0526597ee23a.png align="center")

## Introduction 👋🏿👋🏿👋🏿

Welcome to this interesting series on "*Enhancing Your React Native App.*" 🎉🎉. In the last article, we saw what was needed for a developer interested in building mobile apps using React Native. We also saw that React Native could be used to build cross-platform applications. As we continue to build interesting mobile apps, we seek ways to elevate our creations' visual appeal and user experience.

## Why use custom fonts in apps? 🤷🏿🤷🏿🤷🏿

In building mobile apps, understanding how to implement custom fonts in our apps can greatly enhance the aesthetics and branding of our apps. Using custom fonts in our apps infuses personality, professionalism, and style into our interfaces, elevating them to exceptional.

In this article, we will learn how to use custom fonts to make our app visually captivating and leave a lasting impression on the users.

## Exploring resources for custom fonts 📒👨🏿‍💻

Here is a list of websites where you can find custom fonts for your personal or commercial projects:

* [*Google fonts*](https://fonts.google.com/)
    
* [*Font squirrel*](https://www.fontsquirrel.com/)
    
* [*FFont*](https://www.ffonts.net/)
    
* [*Free script fonts*](https://www.freescriptfonts.net/)
    
* [*1001 free fonts*](https://www.1001freefonts.com/), etc
    

## Using custom fonts in our React Native app 🔡🔠

[Getting started with React Native Guide](https://reactnative.dev/docs/environment-setup) will help us set up your machine for React Native.

After setting up our machine for React Native, the following steps will help us achieve our objective:

PS: The device you are using matters when developing React Native applications. For this article, I am using an Apple Mac device.

1. Uninstall any previously installed global `react-native-cli` package
    
    ```bash
    npm uninstall -g react-native-cli @react-native-community/cli
    ```
    
2. Run the command to create a new React Native project
    
    ```bash
    npx react-native init RNFonts
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708291774815/a5c2a32d-3f84-4ad3-beeb-573f7fd6294a.jpeg align="center")
    
    Navigate into the app directory:
    
    ```bash
    cd RNFonts
    ```
    
3. Download the fonts we need. For this example project, we will be using selected fonts from some of the resources above:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708290317858/2ba5a6d3-153e-4d53-a7f2-36f74c0726b8.png align="center")
    
    [`Iceberg - 1001Fonts`](https://www.1001freefonts.com/iceberg-font-52000.font)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708290663994/0d96592e-6d5c-4a38-b706-2470ae42d1da.png align="center")
    
    [`Orange Juice - 1001Fonts`](https://www.1001freefonts.com/orange-juice.font)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708290799084/b1b86710-6323-40f5-b0c6-95efeb7a0b24.jpeg align="center")
    
    [`Gravity Sucks - FFonts`](https://www.ffonts.net/Gravity-Sucks1.font#)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708290980387/9986ee87-b0b9-46b9-b5ab-af02c1ba45e1.jpeg align="center")
    
    [`Protest Revolution - Google fonts`](https://fonts.google.com/specimen/Protest+Revolution)
    
    **PS**: *Ensure that the downloaded fonts are in the*`.ttf`*format.*
    

### Importing custom fonts in Android

To use the custom fonts on an Android device,

1. Navigate to the main directory:
    
    ```bash
    cd ./android/app/src/main
    ```
    
2. Create a directory called `assets/fonts`
    
    ```bash
    mkdir assets/fonts
    ```
    
    You should have something like this:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708292792510/767fe415-13e6-487c-8c14-e0d3c3bb16d5.jpeg align="center")
    
3. Move all the custom fonts to the `assets/fonts` folder
    
    Ensure that you rename the files into a name of your choice, e.g. I renamed the `orange-juice 2.0` into `orange-juice`.
    
    It should look like this:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708294298128/3fba7445-4a36-4c5a-a12d-a163d2379c04.jpeg align="center")
    
4. Our font is ready to use on your Android device.
    

### Importing custom fonts in iOS

To use custom fonts in our iOS devices, we'll follow the steps below

1. Navigate to the iOS directory/folder and create a directory/folder called `fonts`
    
    ```bash
    cd ios/
    mkdir fonts
    ```
    
2. Let's copy our downloaded fonts into the `fonts` directory. Ensure they have the same name as we used in the case of Android.
    
    We should have this:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708296919724/74641ce6-4e90-4051-b238-5e1384818703.png align="center")
    
3. Next, we open the `RNFonts.xworkspace` file using Xcode.
    
4. After opening this project on Xcode, on the left-hand side, we click on the project name and select the option "Add files to **RNFonts**".
    
    We should have something like this:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708297177790/4355f1f9-e518-4708-90f2-9e3c2d1a2551.png align="center")
    
5. Next, we select the `fonts` directory that we have created. Remember to select **Create Folder references** from below and click **Add**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708297336671/7045836a-22f4-4524-be48-07345a256722.png align="center")
    
6. Next, we click the **project name - RNFonts** on the left top, and select the project name on **TARGETS**. Click the **Info** tab on the top menu to see `Info.plist`. When you hover over the properties in the `Info.plist` file, we will see a "plus" button and add "**Fonts provided by application"** and **font files** to the `Info.plist`file.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708298179885/a2e6738d-3ffb-4981-bffb-9e5086cda799.png align="center")
    
    After adding it we should have this:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708298542272/2a597cd3-ca7d-42e7-9559-974fa703464b.png align="center")
    
    Or we can just navigate to the `Info.plist` file in the directory `ios/RNFonts/Info.plist` on our **VSCode** and add the font files directly into it.
    
7. ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708298819297/71a73d83-87fe-497d-83f1-332c50f7c5ba.png align="center")
    
    Our fonts should be ready to use on an iOS device.
    

**PS:** *For Orange juice font, it might not display on iOS devices. If we try to use the name that came with the file, i.e.,*`orange juice 2.0.ttf`*or the name we later gave the file*`orange-juice`*it will not still work. This is because iOS uses the "postscript" name of the font.*  
*For me, one of the quick ways to find this out is to check out the name on the iOS font book or better still install the font. Once we install the font, the name of the font is the "postscript" name of that font. For example, after installing the*`orange juice 2.0.ttf`*the font we can see from the image below that the "postscript" name is*`orange juice`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708303000903/20392345-2f85-4260-83ed-a0228b20873d.png align="center")

### Testing our custom fonts on both Android and iOS

1. Jump into the project folder, and open it on **VSCode**
    
    ```bash
    cd RNFonts
    code .
    ```
    
2. Open the `App.tsx` file and replace the content with this:
    
    ```typescript
    import React from 'react';
    import {Linking, Pressable, StyleSheet, Text, View} from 'react-native';
    
    const App = () => {
      return (
        <View style={styles.container}>
          <Pressable onPress={() => Linking.openURL('https://ffonts.net/Gravity-Sucks1.font#')}>
            <Text style={[styles.gravity, styles.universal]}>Gravity Sucks Font</Text>
          </Pressable>
          <Pressable onPress={() => Linking.openURL('https://www.1001freefonts.com/iceberg-font-52000.font')}>
            <Text style={[styles.iceberg, styles.universal]}>Iceberg Font</Text>
          </Pressable>
          <Pressable onPress={() => Linking.openURL('https://www.1001freefonts.com/orange-juice.font')}>
            <Text style={[styles.orangeJuice, styles.universal]}>Orange Juice Font</Text>
          </Pressable>
          <Pressable onPress={() => Linking.openURL('https://fonts.google.com/specimen/Protest+Revolution')}>
            <Text style={[styles.protestRev, styles.universal]}>Protest Revolution Font</Text>
          </Pressable>
        </View>
      );
    };
    
    export default App;
    
    const styles = StyleSheet.create({
      container: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
      },
      universal: {
        marginVertical: 10,
        fontSize: 35,
        color: 'black',
      },
      gravity: {
        fontFamily: 'GravitySucks',
      },
      iceberg: {
        fontFamily: 'Iceberg',
      },
      orangeJuice: {
        fontFamily: 'orange juice',
      },
      protestRev: {
        fontFamily: 'ProtestRevolution-Regular',
      },
    });
    ```
    
3. Start our Metro bundler 💨💨💨
    
    For us to run our project, we need to start the Metro bundler using the command below:
    
    ```bash
    npm run start
    ```
    
4. Starting our Android application
    
    To start our Android application, we use the command below to start our application:
    
    ```bash
    npx react-native run-android
    ```
    
    Here is the output of our application on an Android device
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708299312543/120b1d39-3575-4bbf-a001-05f0283557e9.png align="center")
    
5. Starting our iOS application
    
    To run our application on iOS, we run the command below:
    
    ```bash
    npx react-native run-ios
    ```
    
    Here is the output of our application on the iOS simulator
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708303193032/dcef08e0-3f31-4efc-b61a-fc8ed6607442.png align="center")
    

And we have come to the end of this article on using custom fonts. If you have a challenge following the steps, you can ask your questions in the comment box.✅✅

![](https://media1.tenor.com/m/VDeODFt482oAAAAC/finished-spongebob-squarepantes.gif align="center")

To receive an update when the article drops, do well to subscribe to my newsletter or follow me on any of the social media platforms.

Twitter 🐦: @[@nwokporo_ebuka](@nwokporo_ebuka)

LinkedIn ⚡: @[@chukwuebuka_nwokporo](@chukwuebuka_nwokporo)

GitHub 🚀: @[@ebukvick](@ebukvick)

Hashnode 📗: @[Nwokporo Chukwuebuka](@codeDaddy)