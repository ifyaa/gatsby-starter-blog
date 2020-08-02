---
title: 파닥파닥강의 
date: "2020-07-29"
description: 파닥파닥강의 
---

![](https://i.ibb.co/vBNxPbC/image.png =150x)
![](https://i.ibb.co/YWLmf0Q/image.png =300x)

![](![image](https://i.ibb.co/x3Mt3D7/image.png =300x)
![](https://i.ibb.co/dfVMPw6/image.png =300x)
![](https://i.ibb.co/YZFknKZ/image.png =300x )
![](https://i.ibb.co/fFr9mqk/image.png =300x)
![](https://i.ibb.co/VD45P2f/image.png =300x)
![](https://i.ibb.co/jWLsqLP/image.png =300x)

![](https://i.ibb.co/BnhDWv2/image.png =300x)
```js
import 'package:flutter/material.dart';
import 'grid_page.dart';
import 'list_page.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'title',
      theme: ThemeData(
        primarySwatch: Colors.red,
      ),
      home: MainPage(),
    );
  }
}


class MainPage extends StatefulWidget{

  @override
  State<StatefulWidget> createState(){
    return _MainPageState();
  }
}

class _MainPageState extends State<MainPage>{

  int _selectedTabIndex = 0;

  @override
  Widget build (BuildContext context){
    return Scaffold(
      appBar: AppBar(
        // leading: Icon(Icons.menu),
      
        title: Text('h5eeeeeead'),
        actions: <Widget>[
          PopupMenuButton<int>(
            icon: Icon(Icons.sort),
            onSelected: (value) {
              if(value == 0) print("aaa");
              else if(value == 1) print("bbb");
              else print("ccc");
            },
            itemBuilder: (context) {
              return [
                PopupMenuItem(value: 0, child: Text("aaa")),
                PopupMenuItem(value: 1, child: Text("bbb")),
                PopupMenuItem(value: 2, child: Text("ccc")),
              ];
            },
          )
        ],
      ),

      body: _buildPage(_selectedTabIndex),

      bottomNavigationBar: BottomNavigationBar(
       items: <BottomNavigationBarItem>[
         BottomNavigationBarItem(
          icon: Icon(Icons.view_list),
          title: Text('List'),
        ),
            BottomNavigationBarItem(
             icon: Icon(Icons.grid_on),
            title: Text('Grid'),
          ),
        ],
        currentIndex: _selectedTabIndex,
        onTap: (index){                    StatefulWidget로 바꾸고 SetState()한줄만 삽입하면됨
           setState((){   -------------------------------->>>>>>리스트 버튼 선택 
              _selectedTabIndex = index;
              print("$_selectedTabIndex Tab Clicked");
           });

        },
      )
    );
  }
}
##------------------------>>화면전환 
Widget _buildPage(index){
  if(index == 0)
    return ListPage();
    else 
    return GridPage();
}



```
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI5NDg0Nzk4MywtMTgwNjkxMDM4NywtMT
Q3Mzk0MDIyNCw4MDgyODcwMTIsMTQ0NzkyNzE3OV19
-->