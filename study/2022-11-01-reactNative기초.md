---
layout: page
title: "React Native 기초"
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
>expo 설치<br>
🔧 npm install --global expo-cli

>watchman 설치<br>
- 특정 폴더나 파일에 변화가 생기면 특정 동작을 실행하도록 해준다.
🔧 brew install watchman
> 프로젝트 생성<br>
```re
expo init [프로젝트 명] --npm
```
blank 선택

> 프로젝트 시작<br>
```re
expo start
```

## 명령어
view === container<br>

## React Native Packages
- 초기 버전에는 다양한 **API**와 **Component**들이 존재 했지만 현재 각종 버그들로 인해 필요한 것만 남겼다.

 '
💡API: 자바스크립트 코드
💡Component: 화면에 렌더링할 항목

### Third-Party Packages
<a href="https://reactnative.directory/" target="_blank">React Native Directory</a>

#### Storage 구성
react native mmkv storage

<a href="https://github.com/ammarahm-ed/react-native-mmkv-storage" target="_blank">React Native mmkv storage</a>

<a href="https://docs.expo.dev/versions/latest/" target="_blank">Expo Docs</a>

Expo SDK

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
icons.expo.fyi
- Icon Family를 제공

## APIs

## dimentions
- 스크린 사이즈 확인

```js
const { windowWidth, windowHeight } = Dimensions.get("window").width;
```

## Expo Location
🔧 expo install expo-location



## Components

### TouchableOpacity
- 터치 시 투명도를 조절

### TouchableHightlight

[Touchable 더 살펴보기](https://docs.expo.dev/versions/v44.0.0/react-native){:target="_blank"}
