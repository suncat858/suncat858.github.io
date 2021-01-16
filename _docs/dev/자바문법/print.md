---
title: 출력문
category: Java
order: 3
---

### 출력 - println()

println()
```
System.out.println("문자열");
          또는
System.out.println(변수명);
          또는
System.out.println("문자열"+변수명);
```
* 문자열을 출력하기 위해서는 큰따옴표로 묶어줘야 한다.
* 큰 따옴표 없는 것은 모두 변수명으로 인식한다. (입력한 
변수명이 없을 경우 에러발생)
*  문자열과 변수명을 함께 사용할 수 있으나 반드시 '+'로 연결시켜줘야 한다.
* 가로안의 내용을 출력한 후 자동으로 줄바꾸는 기능이 있다.
```java
public class Println {
 
    public static void main(String[] args) {
        //기본 출력문 println()        
        //sysout + 자동완성(ctrl + space)
        
        int number = 10;
        String str = " hello";
        
        System.out.println("hello"); //문자열 출력
        System.out.println(number); //int형 변수 출력
        System.out.println(str); // String형 변수 출력
        System.out.println("내 나이는"+number+"살이야 "); // 문자열 + 변수 출력        
        
    }//main
 
}//class
```
### 형식화된 출력 - printf()

printf()
```
System.out.printf("출력 서식",출력할 내용);
```

* 출력 후 줄바꿈을 하지 않는다. 줄바꿈을 하려면 지시자 '%n'을 넣어줘야 한다.
* 출력하려는 값의 수만큼 지시자도 사용해야 한다.
* 출력될 값과 지시자의 순서는 일치해야 한다.
* 지시자를 제외한 문자는 입력한 그대로 출력된다.

