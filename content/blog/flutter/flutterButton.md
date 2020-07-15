---
title: flutter 
date: "2020-07-15"
	description: flotter 버튼모음.
---
[buttons](https://pythonkim.tistory.com/115)

가장 많이 사용하는 [RaisedButton](https://docs.flutter.io/flutter/material/RaisedButton/RaisedButton.html), 버튼 눌림 기능이 없는 [FlatButton](https://docs.flutter.io/flutter/material/FlatButton/FlatButton.html),  
상단 제목의 왼쪽이나 오른쪽에 주로 들어가는 [IconButton](https://docs.flutter.io/flutter/material/IconButton/IconButton.html)(프린터),  
안드로이드에서 주로 사용하는 공중에 떠있는 듯한 [FloatingActionButton](https://docs.flutter.io/flutter/material/FloatingActionButton/FloatingActionButton.html),  
버튼은 아니지만 버튼처럼 사용할 수 있는 [InkWell](https://docs.flutter.io/flutter/material/InkWell/InkWell.html),  
마지막으로 사진으로 만든 버튼까지.  
  
출처: [https://pythonkim.tistory.com/115](https://pythonkim.tistory.com/115) [파이쿵]
![](https://i.ibb.co/pf3fSrs/Screen-Shot-2020-07-15-at-3-13-39-PM.png)
```js
import 'package:flutter/material.dart';

void main() {
    runApp(MaterialApp(
        title: '버튼 종류',
        home: Scaffold(
            appBar: AppBar(title: Text('버튼 종류'),),
            body: MyApp(),
        ),
    ));
}

class MyApp extends StatelessWidget {
    BuildContext ctx;
    
    @override
    Widget build(BuildContext context) {
        ctx = context;
        return Center(
            child: Column(
                children: <Widget>[
                    RaisedButton(
                        child: Text('RaisedButton', style: TextStyle(fontSize: 24)),
                        onPressed: () => showMessage('RaisedButton'),
                    ),
                    FlatButton(
                        child: Text('FlatButton', style: TextStyle(fontSize: 24)),
                        onPressed: () => showMessage('FlatButton'),
                        color: Colors.green,
                        textColor: Colors.white,
                    ),
                    IconButton(
                        icon: Icon(Icons.print),
                        onPressed: () => showMessage('IconButton'),
                    ),
                    FloatingActionButton(
                        child: Icon(Icons.add),
                        onPressed: () => showMessage('FloatingActionButton'),
                    ),
                    InkWell(
                        child: Text('InkWell', style: TextStyle(fontSize: 24)),
                        onTap: () => showMessage('InkWell'),
                    ),
                    InkWell(
                        child: Image.asset('images/family_1.jpg', width: 120, height: 120),
                        onTap: () => showMessage('ImageButton'),
                    ),
                ],
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
            ),
        );
    }
    
    void showMessage(String msg) {
        final snackbar = SnackBar(content: Text(msg));

        Scaffold.of(ctx)
            ..removeCurrentSnackBar()
            ..showSnackBar(snackbar);
    }
}


출처: https://pythonkim.tistory.com/115 [파이쿵]
```
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NTAwNjMwODNdfQ==
-->