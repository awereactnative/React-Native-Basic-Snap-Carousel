# React-Native-Basic-Snap-Carousel
# Introduction

In this, we will discuss how to integrate Carousel in a React Native application.
Carousels are widely used by many big websites, such as Amazon, Flipkart, etc. The same design element has been ported to mobile apps like Tinder, which uses swipe animation.

# Demo

![Hero_Image](https://user-images.githubusercontent.com/86215353/181407756-fe234169-4f24-499e-8755-3aaa8fb7cbe9.gif)


# Installation
```
npm i react-native-snap-carousel
```

# Example
```js
import * as React from 'react';
import { Text, View, SafeAreaView } from 'react-native';
import Carousel from 'react-native-snap-carousel';

export default class App extends React.Component {

    constructor(props){
        super(props);
        this.state = {
          activeIndex:0,
          carouselItems: [
          {
              title:"Item 1",
              text: "This is text area for Item 1",
          },
          {
              title:"Item 2",
              text: "This is text area for Item 2",
          },
          {
              title:"Item 3",
              text: "This is text area for Item 3",
          },
          {
              title:"Item 4",
              text: "This is text area for Item 4",
          },
          {
              title:"Item 5",
              text: "This is text area for Item 5",
          },
        ]
      }
    }

    _renderItem({item}){
        return (
          <View style={{
              backgroundColor:'lightgreen',
              borderRadius: 5,
              height: 250,
              padding: 50,
              marginLeft: 25,
              marginRight: 25, }}>
            <Text style={{fontSize: 30}}>{item.title}</Text>
            <Text>{item.text}</Text>
          </View>

        )
    }

    render() {
        return (
          <SafeAreaView style={{flex: 1, backgroundColor:'black', paddingTop: 250, }}>
            <View style={{ flex: 1, flexDirection:'row', justifyContent: 'center', }}>
                <Carousel
                  layout={"default"}
                  ref={ref => this.carousel = ref}
                  data={this.state.carouselItems}
                  sliderWidth={300}
                  itemWidth={300}
                  renderItem={this._renderItem}
                  onSnapToItem = { index => this.setState({activeIndex:index}) } />
            </View>
          </SafeAreaView>
        );
    }
}

```

# Tutorial

Coming Soon...
