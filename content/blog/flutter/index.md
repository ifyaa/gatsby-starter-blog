---
title: flutter
date: "2020-07-06"
description: flotter 이야기를 합니다.
---


**[강의동영상](https://www.youtube.com/watch?v=LzG-vkmpDIc)(https://www.youtube.com/watch?v=LzG-vkmpDIc)




```ls
 flutter create my_app**

```

###시작

```js
맥에서
 open -a Simulator
```

![](https://i.ibb.co/ZXGjLww/flutter-000.png)
```js
import 'package:flutter/material.dart';

void main(){
  runApp(                                  // 앱을 실행
    Center(                                // 화면 중앙
      child: Text(                         // 중앙 내부에 텍스트 삽입
        "IFYAA",               
        style:  TextStyle(fontWeight:  FontWeight.bold),
        textDirection: TextDirection.ltr,  // 텍스트는 왼쪽에서 오른쪽을 기술
      ),
    )
  );
}
```
인스타그램 강의 동영상
[enter link description here](https://edu.goorm.io/learn/lecture/11572/flutter-%EC%9E%85%EB%AC%B8-%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-ios-%EA%B0%9C%EB%B0%9C%EC%9D%84-%ED%95%9C-%EB%B2%88%EC%97%90/lesson/466231/%ED%99%94%EB%A9%B4-%EC%84%A4%EA%B3%84-%EB%BC%88%EB%8C%80-%EC%9E%91%EC%84%B1)
시작 합니다
![](https://i.ibb.co/0C1pb5d/2020-07-06-9-31-04.png)
```js
import 'package:flutter/material.dart';

class TabPage extends StatefulWidget {
  @override
  _TabPageState createState() => _TabPageState();
}

class _TabPageState extends State<TabPage> {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Text('tab page'),
    );
  }
}

```
![](https://i.ibb.co/QrLjS6J/2020-07-06-9-26-05.png)
![](https://i.ibb.co/BncVxvC/2020-07-06-9-24-45.png)
```js
import 'package:flutter/material.dart';

class TabPage extends StatefulWidget {
  @override
  _TabPageState createState() => _TabPageState();
}

class _TabPageState extends State<TabPage> {
  @override
  Widget build(BuildContext context) {
    // return Container(
    //   child: Text('tab page'),
    // );
    return Scaffold(
      bottomNavigationBar: BottomNavigationBar(
        items: <BottomNavigationBarItem>[
          BottomNavigationBarItem(icon: Icon(Icons.home), title: Text('Home')),
          BottomNavigationBarItem(
              icon: Icon(Icons.search), title: Text('Search')),
          BottomNavigationBarItem(
              icon: Icon(Icons.account_circle), title: Text('Account')),
        ],
      ),
    );
  }
}
```
![](https://i.ibb.co/GM9NwFv/2020-07-06-9-19-34.png)
![](https://i.ibb.co/t4byD8B/2020-07-06-9-39-00.png)
![](https://i.ibb.co/7tvqMJ8/2020-07-06-9-45-12.png)
![](https://i.ibb.co/2jZgZbf/2020-07-06-9-48-20.png)
![](https://i.ibb.co/TYG9kc5/2020-07-06-9-50-35.png)
![](https://i.ibb.co/nsmbYhQ/2020-07-06-9-53-09.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzYxMzI3Mzk5LDk4NzkxNjg4NywtNzg1Mz
Q0MzMwLC0xNTg5MTU1NjY3LC0xMjk4NjE5MTg1LC0yNzI2NjM4
MzUsMTg3NTgwNDU3LC01NTc0NDE3MzksLTE5MzEyMjA0ODhdfQ
==
-->