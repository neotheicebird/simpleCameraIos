# Instructions

## Create Expo Project (5mins)

```
nvm use 20

npm install -g expo-cli

# create new project, choose Typescript Blank template
npx expo init simple-camera-expo

cd simple-camera-expo

# tunnel using ngrok, useful when PC and phone are in different networks
npx expo start --tunnel

# expo start shows the url and a QR code
```

To connect on iOS device, download Expo Go app. Open camera app to scan above QR code and setup dev environment.

## Create a react-native app and copy App.js to Expo's App.js (2mins)

Expo's app.js is minimal. React native default template has more features to quickly go through. It also adds an `/ios` and `/android` directory, which has build files. Ofcourse expo has its own way to take care of this, but we wish to add a Github Actions based ios build system and not rely on Expo builds which are a bit pricey.

```
cd <different-directory>

npx react-native init <example>

cd <example>

cp <example>/App.tsx ../simple-camera-expo/App.tsx

# copy the ios directory
cp <example>/ios ../simple-camera-expo/
```

## Add camera module and take pictures

refer to expo camera docs

## Add camera module and take pictures

refer to expo-camera docs

## Configure project

The project needs to be configured with EAS, before builds, even local one can be made. Make sure you have signed up for an EAS account.

```
eas build:configure
```

### Notes

`bundleIdentifier`: A unique ID in apple registry, apple suggests using reverse of website name, for example if the app is for google.com, then the bundleIdentifier could be "com.google"
