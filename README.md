# @nghinv/react-native-switch

React Native Switch Library

---

[![CircleCI](https://circleci.com/gh/nghinv-software/react-native-switch.svg?style=svg)](https://circleci.com/gh/nghinv-software/react-native-switch)
[![Version][version-badge]][package]
[![MIT License][license-badge]][license]
[![All Contributors][all-contributors-badge]][all-contributors]
[![PRs Welcome][prs-welcome-badge]][prs-welcome]

<p align="center">
<img src="./assets/demo.png" width="300"/>
</p>

## Installation

```sh
yarn add @nghinv/react-native-switch
```

or 

```sh
npm install @nghinv/react-native-switch
```

- peerDependencies

```sh
yarn add react-native-gesture-handler react-native-reanimated
```

## Usage

```js
import React, { useState } from 'react';
import { View, Text, StyleSheet } from 'react-native';
import Switch from '@nghinv/react-native-switch';

function App() {
  const [enable, setEnable] = useState(true);

  return (
    <View style={styles.container}>
      <View style={styles.row}>
        <Text style={styles.title}>Switch</Text>
        <Switch 
          value={enable} 
          onChange={(value) => setEnable(value)} 
        />
      </View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
  },
  row: {
    flexDirection: 'row',
    alignItems: 'center',
    justifyContent: 'space-between',
    padding: 16,
  },
  title: {
    fontSize: 16,
  },
});

export default App;
```

# Property

| Property | Type | Default | Description |
|----------|:----:|:-------:|-------------|
| size | `Number` | `27` |  |
| thumbColor | `String` | `white` |  |
| trackColor | `TrackColorProperty` |  |  |
| disabled | `Bool` | `false` |  |
| value | `Bool` | `false` |  |
| onChange | `(value: boolean) => void` | `undefined` |  |
| style | `ViewStyle` | `undefined` |  |
| progress | `Animated.SharedValue<number>` | `undefined` |  |


## TrackColorProperty

| Property | Type | Default | Description |
|----------|:----:|:-------:|-------------|
| false | `String` | `rgba(120, 120, 120, 0.3)` |  |
| true | `String` | `#31D158` |  |

---
## Credits

- [@Nghi-NV](https://github.com/Nghi-NV)

[version-badge]: https://img.shields.io/npm/v/@nghinv/react-native-switch.svg?style=flat-square
[package]: https://www.npmjs.com/package/@nghinv/react-native-switch
[license-badge]: https://img.shields.io/npm/l/@nghinv/react-native-switch.svg?style=flat-square
[license]: https://opensource.org/licenses/MIT
[all-contributors-badge]: https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square
[all-contributors]: #contributors
[prs-welcome-badge]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square
[prs-welcome]: http://makeapullrequest.com
