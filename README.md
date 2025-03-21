# Today I Learned

### 수평적 사고 : 같은 대상을 봐도 여러 가지 생각이 나오는데 이것을 수평적 사고라고 한다.<br>
&nbsp;&nbsp;&nbsp;&nbsp;ex) 자전거를 보고 그냥 자전거라고 생각하는 경우도 있고 인생에 비유하는 경우도 있다.

## @ Dart 언어란?
▶ Google에서 만든 JavaScript와 유사하지만 다른 정적 언어<br>
&nbsp;&nbsp;&nbsp;&nbsp;(Java - 클래스 및 매서드 구문 유사 / C# - 비동기 프로그래밍 async, await 등 유사)<br><br>
▶JavaScript의 동적 언어의 성능, 일관성 문제를 보완하기 위해 설계

## ● Dart 언어 - 실습
- **[구구단](./구구단.dart)**
- **[정사각형 출력](./정사각형_출력.dart)**
- **[요일 출력](./요일_출력.dart)**

## ● var 선언
```dart
void main() {
  int a = 5;
  double b = 3.1415;
  String c = '문자열1';
  String d = "문자열2";
  bool e = true;
  num n1 = 10;
  num n2 = 10.25;
  
  bool cond1 = a > 5; // false
  bool cond2 = d == "문자열2";
  bool result = cond1 || cond2;
  
  // 전부 var로 변수 선언 가능
}
```

## ● 상수 final, const, 사칙연산
```dart
//final, const로 설정한 변수는 변경X
void main() {
  final name = '홍길동';
  //name = '임꺽정'; X
  
  const name2 = '임꺽정';
  //name2 = '홍길동'; X
  
  // +, -, *, /
  var a = 10;
  var b = 5;
  var result = a % b;
  print(result);
  print(result is int);
  print(result is double);

  // /:나누기, double형으로 반환
  // ~/:몫, int형으로 반환
  // %:나머지, int형으로 반환
}
```

## ● 숫자 관련, 비교
```dart
// ++/-- 증감 연산자
// 후위 연산(시작하면서 계산):x++,x--
// 전위 연산(계산하면서 시작):++x,--x
void main() {
  var v = 5;
  v++;
  print(v);
}
```
```dart
// 비교
void main() {
  var a = 5;
  var b = 6;
  
  var c1 = a == b;
  var c2 = a != b;
  var c3 = a < b;
  var c4 = a > b;
  var c5 = a >= b;
  var c6 = a <= b;
  
  var result = [c1, c2, c3, c4, c5, c6];
  print(result);

  // and(%%), or(||), not(!)
  var isA = true; // 아침식사
  var isB = true; // 점심
  var isC = true; // 저녁
  
  //오늘 밥 먹었나
  var c = isA || isB || isC;

  // 변수 상태 확인
  var v = 5;
  print(v is int); // v 는 정수
  print(v is double); // 5 = 5.0
  print(v is String);
  print(v is bool);
  
  int a = 5;
  num b = a as num;
  print(b);
}
```

## ● 함수 선언
```dart
// print2 함수를 만들고 인자로 주어진 문자열로 다음처럼 출력하는 함수를 만들어 사용하자.
//
//print2("Hello World");
//출력:*Hello World*

void main() {
  print2('Hello World');
}

void print2(String message) {
  //print('*$message*');
  print('*' + message + '*');
}
```

## ● List
```dart
void main() {
  var lottoNums = [5, 6, 11, 13, 17, 21];
  //print(lottoNums is List); 리스트인지 확인
  
  lottoNums.forEach((num) => print(num));
}
```

## ● if
```dart
void main() {
  var score = 88;
  if (score >= 90) {
    print('A');
  } else if (score >= 80) {
    print('B');
  } else if (score >= 70) {
    print('C');
  } else if (score >= 60) {
    print('D');
  } else {
    print('F');
  }
}
```

## ● for
```dart
void main() {
  var items = ['짜장', '라면', '볶음밥'];
  
  for (var i = 0; i < items.length; i++) {
    print(items[i]);
  }
  
  print('');
  
  for (var item in items) {
    print(item);
  }
  
  print('');
  
  items.forEach((item) => print(item));
}
```
=======
>>>>>>> 81640926a82d2a074c44a2c766d4b36de3578d87
