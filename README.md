# Renton Technical College CSI-248
<br />    

<div align="center">  
    <img src="logo.jpg" alt="Logo">
    <h3 align="center">Guided Activity 5</h3>
</div>

This repository is a part of CSI-248 at Renton Technical College.

## Guided Activity 6

## Setup Expo - If you have already done this in class you may skip this step

1. Sign up for an account at https://expo.dev/
2. Install Expo Go on your mobile device in the Apple App Store or Google Play Store
3. Sign in to the Expo Go App using your account you made at expo.dev

## Clone the repo

1. Clone the repository to your local machine. (Do not use OneDrive for assignments in this course!)
2. Make note of the folder where you cloned the repository.
3. After you have cloned this repository navigate to your local repository using the cd command.
4. Open the repository in Visual Studio Code by typing `code .`
5. Create a folder to store the requested Screenshots for this assignment.

## Creating your first react-native project
1. Open the terminal in Visual Studio Code and create a new expo app by running `npx create-expo-app custom-button`
2. Run `cd custom-button`
3. You are now in the root project of the folder. Notice that there are some files that look familiar such as package.json and App.js
4. Run `npx expo install react-dom react-native-web @expo/webpack-config` to enable react-native for web
5. Run `npx expo start` to launch the project. You will see a QR Code in the terminal.
6. Type `w` to launch the app in a web browser. You should now see your app running in your default browser.
7. Scan this QR Code with the Camera on IOS or using the Expo Go app on Android and you App will launch on your device.


## Understanding Pressable

1. Replace App.js with the following:

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/ef7bb326-ee5e-48c1-ba25-59e016f017c2)

2. The button component works for quick projects but it is very limited in what can be done with it. For example the background color can be change but not the text color.
3. Button has a nice effect when it is clicked on however that effect cannot be customized.
4. Make the following changes to App.js

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/38627306-4b68-45c2-af23-f3326f7e00f6)

5. TouchableOpacity offers the effect when a button is clicked as well as the ability to change both background color and the text color. Notice that the text inside of the button is its own component. There is no title prop used.

6. Change the TouchableOpacity component to a Pressable.

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/15855f52-ce5c-4766-98f1-ce4442ed5101)

7. Now noticed when you click on the buttons there is no effect to show that is has been clicked on. It is possible to create this effect with Pressable, however we much create it ourselves.

8. Notice what happens if you add an opacity to the btn style:

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/3cd35233-5cec-4ed0-b5ff-d04654710ae2)

10. The buttons will appear faded. We can make this happen on press by supplying a callback function to the style prop.
11. Delete the `opacity: 0.5` from the btn style.
12. The style prop of the pressable is now supplying a callback function, that callback function is taking in a parameter called pressed.
13. pressed will be true when the button is pressed or false otherwise.

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/f3c48249-f1ad-48c0-975d-edd36110ff82)

14. Using this pressed parameter we can supply an array of styles to the style prop:

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/401b41f2-ac4e-4a47-af9d-7cefe80c3e69)

15. Notice now when you click the button you will see the opacity and background change
16. Pressable has multiple press events that you can use.
onHoverIn
onHoverOut
onLongPress
onPress
onPressIn
onPressOut

17. Lets add a press and a longPress event:

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/efc5a2f4-c865-484a-8cb1-8784025e021b)

18. Click your pressable and take a screenshot of the output
19. Click and hold on your pressable and take a screenshot of the output.

## Create a custom button component
1. As you can see, this is quite a lot of code to repeat everywhere that you want a button.
2. It is common practice to create a custom button for your app that you can re-use.
3. Typically you will pre-define a few different colors within the component and then select which one you want rendered using a prop.
4. Common button types are primary, secondary, submit, warning and danger. 
5. Create a CustomButtom component that takes the following props
  onPress, //callBack for press
  onLongPress, //callback for longpress
  title, //this will be the text of the button
  type = "primary", // this will change the appearance of the button and the text, default is primary
  disabled = false, //buton is not disabled by default
  pressedOpacity = 0.5 //default opacity when pressed
6. You can chose whatever colors you like for the different types of buttons. Here is an example

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/474e9551-f77e-4f9e-b0cf-7ad82c9f0775)

7. Once complete render the custom buttons in App.js and take a screenshot.
8. Notice how much easier it is to use these buttons than the Pressable element we made earlier.

![image](https://github.com/EmeryCSI/csi248-guidedactivity5/assets/102991550/e6fdd0ce-deee-4ad9-a601-49f6372aabb4)

9 Since you made the component yourself you have full control over its appearance, however you also have the ease of use of the built-in Button component.

10. Take a screenshot of your final functioning app add it to the screenshots folder.
11. `git add .`
12. `git commit -m "Assignment Complete"`
13. `git push`

If you have any questions about this assignment please reach out to myself or our TA for this course. 
https://expo.dev/
