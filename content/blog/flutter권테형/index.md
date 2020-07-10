---
title: fluttter_net
date: "2020-07-11"
description: "권태형"
---

[강의](https://taebbong.github.io/2020/03/21/2020-03-21-bbongflix-lec01-post/)

```js
// lib/main.dart
import 'package:flutter/material.dart';
import 'package:netflix_clone_lecture_note/widget/bottom_bar.dart';

void main() => runApp(MyApp());

class MyApp extends StatefulWidget {
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  TabController controller;
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Bbongflix',
      theme: ThemeData(
        brightness: Brightness.dark,
        primaryColor: Colors.black,
        accentColor: Colors.white,
      ),
      home: DefaultTabController(
        length: 4,
        child: Scaffold(
          body: TabBarView(
            physics: NeverScrollableScrollPhysics(),
            children: <Widget>[
              Container(
                child: Center(
                  child: Text('home'),
                ),
              ),
              Container(
                child: Center(
                  child: Text('search'),
                ),
              ),
              Container(
                child: Center(
                  child: Text('save'),
                ),
              ),
              Container(
                child: Center(
                  child: Text('more'),
                ),
              ),
            ],
          ),
          bottomNavigationBar: Bottom(),
        ),
      ),
    );
  }
}
```


![Chinese Salty Egg](./salty_egg.jpg)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAxNzI3OTAxM119
-->