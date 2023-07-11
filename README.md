# ⚡️React Native Lab 1 instructions

Welcome to this crash course on how to create a mobile app with React Native! Today's lab has three parts.

# Part 1: Set Up

*This heavily adapts content from [Expo Docs](https://docs.expo.io/get-started/installation/) and [React Native Docs](https://reactnative.dev/docs/environment-setup)*.

### 1. ✨ A quick overview

We'll be using the following tools from Expo to develop apps:

1. a command line app called Expo CLI to initialize and serve your project
2. VSCode as our text editor
3. either Expo Go, which allows us to open our projects on the phone, or any web browser to open the project on the web.

> **FYI**: We'll be using `yarn` instead of `npm` as our package manager; you can read more about the difference [here](https://www.sitepoint.com/yarn-vs-npm/)! In short, `yarn` is becoming more popular.
> 

### 2. 👾 In your terminal run the following commands:

```
brew install watchman
```

> **FYI:** Watchman was developed by Facebook to watch for file changes. It'll help with hot reloading later!

Make sure your yarn version is 1.22.19:
```bash
$ yarn -v
1.22.19
```

<details>
  <summary>(If you see 3.6.0 or 3.6.1, expand to see how to downgrade)</summary>
  
(As of July 2023) React Native isn't compatible with any yarn versions other than `1.22.19`, so even though you have a more recent version, you'll need to downgrade. We want yarn `>=3.6.1` for our React projects, but not for React Native. The global/default version of yarn should be `1.22.19` and upgrading yarn to `3.6.1` with `yarn set version stable` should be done on a per-project basis only.

Start by removing the yarn project configuration from your user root (aka `~`) folder. (Hopefully this is the only place you'll need to do this, but if you try `yarn -v` and get something other than `1.22.19` later, you'll need to hunt for these files in other parent folders.)

```bash
cd ~

rm -rf node_modules .yarnrc .yarnrc.yml package.json yarn.lock
```

Now that those files are cleared out, run `yarn -v`. You should get `1.22.19`, but if you get an error, run `brew install yarn` to reinstall.
  
</details>

### 3. 📲 On your phone, download the Expo Go app:

[🤖 Android Play Store - Android Lollipop (5) and greater.](https://play.google.com/store/apps/details?id=host.exp.exponent)

[🍎 iOS App Store - iOS 11 and greater.](https://search.itunes.apple.com/WebObjects/MZContentLink.woa/wa/link?path=apps%2fexponent)

**Set up an account if needed!**

### 4. 👾 In your terminal, initialize an Expo project:

```
cd desktop/sea/
# or, wherever you want your files to be located!
 
yarn create expo
```

You might be asked to choose a template. For now, let's go with Managed workflow -> blank.

Then, navigate to the project directory and open up the files in VSCode.

```
cd my-app

code .
```

### 5. 👾 Finally, let's launch the project on both web and mobile.

Start the development server with the following:

```
yarn expo start
```

This should open up something in your web browser! In the future, you only need to run this command to get your project running.

![https://user-images.githubusercontent.com/26272095/124739226-8622f800-dece-11eb-9006-85771624dff2.png](https://user-images.githubusercontent.com/26272095/124739226-8622f800-dece-11eb-9006-85771624dff2.png)

✅ Click "Run in web browser" and you should see a blank screen with the words "Open up App.js to start working on your app!"

✅ Try scanning the QR code with your Expo app (on Android) or Camera (on iPhone) to see the same screen on your phone.

✅ Here's a reference for all of the files in your new app. Go through each one and check them out so you know what is inside. 

- .expo folder = contains configuration information for your machine
- .expo-shared folder = contains info about asset optimization
- **assets folder = contains assets for project (images, icons, fonts, videos)**
- node_modules folder = contains dependencies of project
- .gitignore file = specifies files that Git should ignore
- **App.js file = code to configure our app**
- app.json file = metadata
- babel.config.js file = configuration of how JS code is compiled
- package.json file = manages dependencies
- yarn.lock file = more info about dependencies (stored by Yarn)
- Yarn = package manager

> **FYI** from the Expo Docs: "When you run `yarn expo start`, Expo CLI starts Metro Bundler, which is an HTTP server that compiles the JavaScript code of our app using Babel and serves it to the Expo app. It also pops up Expo Dev Tools, a graphical interface for Expo CLI."
> 

### 6. 👾 Make your first change.

Open up `App.js` in VSCode.

Change the text on line 8 to whatever you want. You should see it update on your device automatically.

Woohoo! You got your first mobile app running.



# Part 2: Components

✨We're going to learn about React Native components in baby steps. Remember, 

- Components are building blocks
- View, Text, and Style are React Native Core Components. There are also Community Components (made by React Native community members, that you can find on github or through a quick google search) and Expo-specific Components.
- The style property is passed into a component and dictates the component’s size, color, alignment, spacing, etc..
- Style Classes let us define styles and StyleSheet lets us organize styles, much like CSS!
- Flex properties let us build flexible and well-spaced layouts

🚧  Note: instead of trying the examples on Snack, go ahead and make the changes in VSCode to the project you just created in the setup.

### 1. 🌈 [Styling text](https://docs.expo.io/tutorial/text/)

### 2. 👾 [Adding an image](https://docs.expo.io/tutorial/image/)

### 3. 👇🏼 [Creating a button](https://docs.expo.io/tutorial/button/)

### 4.  🌠 [Picking an image](https://docs.expo.io/tutorial/image-picker/)

# Part 3: Make an app about yourself.

## First, fork and clone this lab repo:
### To run 
1. Fork this repo! 
2. Git clone the forked repo. 
3. In terminal, move to the project folder then run `yarn`
4. Then launch the project with `yarn expo start` 

## Then try to complete the following:

- ✅ **Change `App.js` to make a mini-app about yourself!**
- ✅ **Can you add more Views to the page to create another text subsection?**
- ✅ **Can you add new styling to Text and View?**
- Check out this documentation of the [StyleSheets](https://reactnative.dev/docs/style) and [Flexbox](https://reactnative.dev/docs/flexbox)
- Helpful View styling props: `backgroundColor, flex, justifyContent, alignContent, padding`, …
- Helpful Text styling props: `color, fontSize, fontWeight, textAlign, padding`,****

## Take a screenshot of your app & add to the Google Classroom Assignment [React Native Lab 1](https://classroom.google.com/c/NTAwNzM2MDgwMzgy/a/NDk2ODYxNDA4NzA5/details)

# Part 4: Managing State and Props

**To understand the basic structure of a React Native app, you need to understand some of the basic React concepts, like JSX, components, state, and props.**

[Learn the Basics · React Native](https://reactnative.dev/docs/tutorial)

**Check out this React Native tutorial BUT do not worry about the "Hello Classes" example at the very end. The reason for this is that we will only be talking about functional components, not class components.**


### Credits
Credit for this lab goes to the [teaching team of CS47 at Stanford, 2021](https://docs.google.com/presentation/d/1I8-SL_rWhyWzau3azI54fmRsq66Qe-QY0EsgRrfbf5g/edit#slide=id.gae5ac78f08_10_0)!
