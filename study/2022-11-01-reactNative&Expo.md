---
layout: page
title: "React Native with Expo"
author: author1
comments: true
description: >
hide_description: true
sitemap: true
---

1. this unordered seed list will be replaced by toc as unordered list 
{:toc}

# React Native
- User와 운영체제(IOS, Android) 사이에 있는 인터페이스.
- shell과 같다
- 운영체제와 소통할 수 있게 한다.

## 동작 방식
React Native -(bridge)- Android/IOS


## 브라우저와의 차이점

<hr>

## 사용하기(with Mac🍎)
expo 설치<br>
> 🔧 npm install --global expo-cli

watchman 설치<br>
- 특정 폴더나 파일에 변화가 생기면 특정 동작을 실행하도록 해준다.
> 🔧 brew install watchman

프로젝트 생성 후 blank 시작<br>
```re
expo init [프로젝트 명] --npm
```

프로젝트 시작<br>
```re
expo start
```

## 명령어
view === container<br>

## React Native Packages
- 초기 버전에는 다양한 **API**와 **Component**들이 존재 했지만 현재 각종 버그들로 인해 필요한 것만 남겼다.

💡API: 자바스크립트 코드<br>
💡Component: 화면에 렌더링할 항목

### Third-Party Packages
<a href="https://reactnative.directory/" target="_blank">React Native Directory</a>

#### Storage 구성
react native mmkv storage

<a href="https://github.com/ammarahm-ed/react-native-mmkv-storage" target="_blank">React Native mmkv storage</a>

<a href="https://docs.expo.dev/versions/latest/" target="_blank">Expo Docs</a>

## Style
### Flex Box
> View === flexContainer
// column이 default이다.

- flex
원하는 비율대로 box를 설정할 수 있다.
```js
<View style={{ flex: 1 }}>
  <View style={{ flex: 1, backgroundColor: "tomato" }}></View>
  <View style={{ flex: 1.5, backgroundColor: "teal" }}></View>
  <View style={{ flex: 1, backgroundColor: "orange" }}></View>
</View>
```

### ScrollView
- 스크롤 바 기능을 제공

```js
<ScrollView style={styles.weather}>
  <View style={styles.day}>
    <Text style={styles.temp}>27</Text>
    <Text style={styles.description}>Sunny</Text>
  </View>
  <View style={styles.day}>
    <Text style={styles.temp}>27</Text>
    <Text style={styles.description}>Sunny</Text>
  </View>
  <View style={styles.day}>
    <Text style={styles.temp}>27</Text>
    <Text style={styles.description}>Sunny</Text>
  </View>
</ScrollView>
```

⚠️ scrollView에서 style을 적용하려면 **style** 대신 **contentContainerStyle**을 사용해야 한다.

#### horizontal (props)
- 스크롤을 수평으로 변경

#### pagingEnabled (props)
- 스크롤이 자유롭지 못하지만 페이지가 생김

#### showHorizontalScrollIndicator
- 수평 스크롤 시 스크롤 표시

### Icons
- Icon Family를 제공
icons.expo.fyi
<hr>

## React Native APIs

### dimentions
- 스크린 사이즈 확인

```js
const { windowWidth, windowHeight } = Dimensions.get("window").width;
```

### Alert

#### destructive

## React Native Components

### TouchableOpacity
- 터치 시 투명도를 조절

### TouchableHighlight
- **TouchableOpacity**와 비슷하지만 하이라이트 효과가 있음

### TouchableWithoutFeedback
- **TouchableHighlight**와 비슷하지만 애니매이션은 존재하지 않음
<s>애니메이션이 없다고 하나 사용 시 애니메이션이 있었다.</s>

### Pressable
- **TouchableOpacity** 대신 사용되며 더 많은 기능과 섬세한 설정을 제공

### TextInput
- 앱에서 키보드를 통해 텍스트를 입력하기 위한 요소

#### props: onChangeText
- 입력하는 문자를 보여줌

#### props: keyboardType
>> 키보드 형식을 변경
- email-address
- url
- web-search

#### props: returnKeyLabel
return 버튼의 placehorder를 설정
- go
- next
- search
- send

#### props: secureTextEntry
- 입력 시 표시되는 문자를 숨김

#### props: multiline
>> 원하는 만큼 텍스트 입력 가능
💡 default는 한줄만 입력 가능

[React Native Components 더 살펴보기](https://docs.expo.dev/versions/v44.0.0/react-native){:target="_blank"}
<hr>

# Expo
-
[Expo 살펴보기]("https://docs.expo.dev/"){:target="_blank"}

## Expo SDK
- Expo를 이용하여 앱을 만들 때 필요한 도구

💡 SDK(Software Development Kit): 소프트웨어 개발 키트로써 개발자에게 앱을 제작할 수 있는 기능을 제공 

### AsyncStorage
- string만 담을 수 있는 Storage

```js
🔧 expo install @react-native-async-storage/async-storage
```
```js
import AsyncStorage from "@react-native-async-storage/async-storage";
```

## Expo Location
```js
🔧 expo install expo-location
```

## Object Assign
- 기존에 있던 objectd와 병합

