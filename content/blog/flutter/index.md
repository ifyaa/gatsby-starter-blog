---
title: flutter
date: "2020-07-06"
description: flotter 이야기를 합니다.
---


**[강의동영상](https://www.youtube.com/watch?v=LzG-vkmpDIc)(https://www.youtube.com/watch?v=LzG-vkmpDIc)

인스타그램 강의 동영상
[enter link description here](https://edu.goorm.io/learn/lecture/11572/flutter-%EC%9E%85%EB%AC%B8-%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-ios-%EA%B0%9C%EB%B0%9C%EC%9D%84-%ED%95%9C-%EB%B2%88%EC%97%90/lesson/466231/%ED%99%94%EB%A9%B4-%EC%84%A4%EA%B3%84-%EB%BC%88%EB%8C%80-%EC%9E%91%EC%84%B1)


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
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg3NTgwNDU3LC01NTc0NDE3MzksLTE5Mz
EyMjA0ODhdfQ==
-->