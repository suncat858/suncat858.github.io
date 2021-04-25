---
title: map
category: Java
order: 12
---

### map이란
Map은 리스트나 배열처럼 순차적으로(sequential) 해당 요소 값을 구하지 않고 key를 통해 value를 얻는다. 맵(Map)의 가장 큰 특징이라면 key로 value를 얻어낸다는 점이다

### map 사용법
```java
HashMap<String, Integer> map1 = new HashMap<>();
    map1.put("1", 20);
    map1.put("2", 17);
    map1.put("3", 14);
    map1.put("4", 15);
    map1.put("5", 15);
```

### 다른 자료형

Map 역시 List와 마찬가지로 인터페이스이다. Map 인터페이스를 구현한 Map자료형에는 HashMap, LinkedHashMap, TreeMap등이 있다

### get
key에 해당되는 value값을 얻기 위해서는 다음과 같이 한다.
```java
System.out.println(map.get("people"));
```

### containsKey
containsKey 메소드는 맵(Map)에 해당 키(key)가 있는지를 조사하여 그 결과값을 리턴한다.
```java
System.out.println(map.containsKey("people"));
```

### remove
remove 메소드는 맵(Map)의 항목을 삭제하는 메소드로 key값에 해당되는 아이템(key, value)을 삭제한 후 그 value 값을 리턴한다.
```java
System.out.println(map.remove("people"));
```

### size
size 메소드는 Map의 갯수를 리턴한다.
```java
System.out.println(map.size());
```

### TestMap.java

import java.util.HashMap;
```java
public class TestMap {
    public static void main(String[] args) {
        HashMap<String, String> map = new HashMap<String, String>();
        map.put("people", "사람");
        map.put("baseball", "야구");

        System.out.println(map.get("people"));
        System.out.println(map.containsKey("people"));
        System.out.println(map.remove("people"));
        System.out.println(map.size());
    }
}
```