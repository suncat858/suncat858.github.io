---
title: switch문
category: Java
order: 7
---

### switch/case 문

switch/case 문은 if 문과 비슷하지만 좀 더 정형화된 모습의 제어문이다.

switch/case 문의 구조는 다음과 같다.

```java
switch(입력변수) {
    case 입력값1: ...
         break;
    case 입력값2: ...
         break;
    ...
    default: ...
         break;
}
```

#### switch/case 문 예
```java
public class SwitchDemo {
    public static void main(String[] args) {
        int month = 8;
        String monthString = "";
        switch (month) {
            case 1:  monthString = "January";
                     break;
            case 2:  monthString = "February";
                     break;
            case 3:  monthString = "March";
                     break;
            case 4:  monthString = "April";
                     break;
            case 5:  monthString = "May";
                     break;
            case 6:  monthString = "June";
                     break;
            case 7:  monthString = "July";
                     break;
            case 8:  monthString = "August";
                     break;
            case 9:  monthString = "September";
                     break;
            case 10: monthString = "October";
                     break;
            case 11: monthString = "November";
                     break;
            case 12: monthString = "December";
                     break;
            default: monthString = "Invalid month";
                     break;
        }
        System.out.println(monthString);
    }
}
```
switch문의 입력으로 1이라는 숫자가 올 경우 "January"라는 문자열이 12가 입력으로 올 경우 "December"라는 문자열이 출력되는 예제이다. 위의 예는 month가 8로 고정되어 있기 때문에 "August"라는 문자열이 출력될 것이다.

위 switch문은 month의 값이 1이면 case 1: 문장이 실행되고 2이면 case 2: 문장이, 3이면 case 3: ... 이런식으로 수행되게 된다. 만약 month에 1에서 12사이의 숫자가 아닌 다른 값이 저장되어 있다면 default: 문장이 수행될 것이다.

위와 같이 입력값이 정형화되어 있는 경우 if문보다는 switch/case문을 쓰는것이 가독성에서 좀 더 유리하다.
