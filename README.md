# Installing Fonts

Download Roboto font: https://fonts.google.com/?selection.family=Roboto

Install it using the following guide: https://medium.com/react-native-training/react-native-custom-fonts-ccc9aacf9e5e

# Installing package

Yarn: `yarn add react-native-font-weight`

NPM: `npm install react-native-font-weight`



# Initializing Font Manager

Insert the following code into the starting point of the application (usually App.js) 

```js
import FontManager from 'react-native-font-weight';

useEffect(() => {
	FontManager.init();
}, []);
```
# Usage

Use it like you would use fontFamily & fontWeight for iOS (defaults to Roboto on Android)

```jsx
<Text style={{ fontWeight: '300' }}>
	Some Text
</Text>
```

Custom fonts:

```jsx
<Text style={{ fontFamily: 'OpenSans', fontWeight: '300' }}>
	Some Text
</Text>
```

# Notes

- Tested on react: 16.1.8, react-native: 0.60.5
- Only works with default Text field from react-native 
- If corresponding fontWeight file does not exist, it will revert to the default (Roboto, fontWeight: 400)
- fontStyle 'italic' does not work at the moment
