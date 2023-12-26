# Getting Started

## Installation

```bash
npm install react-native-flix-snackbar
```

or using yarn

```bash
yarn add react-native-flix-snackbar
```

## Usage

Wrap your root component in `SnackbarProvider` from `react-native-flix-snackbar`. This will usually be in the `index.js` or `App.js` file. If you have an `Expo` project, you can do this inside the exported component in the `App.js` file.

Example usage `SnackbarProvider`:

```js
import { SnackbarProvider } from 'react-native-flix-snackbar';

export default function App() {
  return (
    <SnackbarProvider>
      <MainApp />
    </SnackbarProvider>
  );
}
```

After you add `SnackbarProvider`, you can show snackbar in all of it's children components using `useSnackbar` hook without importing snackbar component and declaring `ref`.

Example usage `useSnackbar`:

```js
import { useSnackbar } from 'react-native-flix-snackbar';

const { show } = useSnackbar();

// showing snackbar
<TouchableOpacity onPress={() => show('Hi snackbar!')}>
  <Text>Open Snackbar</Text>
</TouchableOpacity>;
```
