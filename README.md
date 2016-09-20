# ![react-native-shake-event-ios](https://storage.googleapis.com/cdn.chessboardradio.com/lab/projects/01-NShakeEventIOS/promo.png)

[![npm package](https://img.shields.io/npm/v/react-native-shake-event-ios.svg?style=flat-square)](https://www.npmjs.org/package/react-native-shake-event-ios)
[![react-native channel on discord](https://img.shields.io/badge/discord-react--native%40reactiflux-738bd7.svg?style=flat-square)](https://discord.gg/0ZcbPKXt5bXsb3os)

Add the shake event on your React Native app, giving to users improved usability. Enjoy!
*(works only on real device)*

## Demo

<a href="https://www.youtube.com/watch?v=mKjkWHto6NQ&feature=youtu.be" target="_blank"><img src="https://storage.googleapis.com/cdn.chessboardradio.com/lab/projects/01-NShakeEventIOS/demo.gif" width="480" height="270" alt="react-native-shake-event-ios"></a>
* [Video Demo](https://www.youtube.com/watch?v=mKjkWHto6NQ&feature=youtu.be)
* [Example App](https://github.com/jadsonlourenco/react-native-shake-event-ios-example)


## Install

```
$ npm install react-native-shake-event --save
```

#### iOS

##### Automatic

`react-native link react-native-shake-event`

##### Manual

1. Add the `RNShakeEvent.xcodeproj` file to your Xcode project [Demo](https://facebook.github.io/react-native/img/AddToLibraries.png);
2. Add the `Products/libRNShakeEvent.a` file to **Build Phases**  [Demo](https://facebook.github.io/react-native/img/AddToBuildPhases.png).

This step is described here: [Linking Libraries](https://facebook.github.io/react-native/docs/linking-libraries-ios.html#content).

#### Android

`react-native link react-native-shake-event`

## Usage

```
import RNShakeEvent from 'react-native-shake-event';

class MyComponent extends React.Component {
  componentWillMount() {
    RNShakeEvent.addEventListener('shake', () => {
      console.log('Device shake!');
    });
  }

  componentWillUnmount() {
    RNShakeEvent.removeEventListener('shake');
  }
}
```

## API

### RNShakeEvent

#### addEventListener('shake', Function)
Start listening the shake event and handle a callback function.

#### removeEventListener('shake', Function)
Stop to listening the shake event, and is recommended to prevent memory leak.

## Issues
1. [Submit here](https://github.com/jadsonlourenco/react-native-shake-event-ios/issues);
2. On *debug mode* this event also handle the **DevMenu**, but works fine on *production*.

## License

MIT © [Chessboard Radio Lab](https://chessboardradio.com)
