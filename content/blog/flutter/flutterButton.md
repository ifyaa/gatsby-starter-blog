---
title: flutter 
date: "2020-07-13"
description: flotter 강의모음.
---

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
eyJoaXN0b3J5IjpbLTUyNzMwMjg0XX0=
-->