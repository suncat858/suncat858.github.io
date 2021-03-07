---
title: service
category: Springboot
order: 1
---

### Service의 처리
```
1) Client 가 Request 를 보낸다.

2) Request URL에 알맞은 Controller 가 수신한다.

3) Controller 는 넘어온 요청을 처리하기 위해 Service 를 호출한다.

4) Service 는 알맞은 정보를 가공하여 Controller 에게 데이터를 넘긴다.

5) Controller 는 Service 의 결과물을 Client 에게 전달해준다.
```

### Controller 에서 Service 호출해서 처리

```java
package com.springboot.practice.controller;

import com.springboot.practice.service.TestService;
import lombok.AllArgsConstructor;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@RestController
@AllArgsConstructor
public class TestController<number5> {
    private TestService TestService;

    @GetMapping(value = "/test")
    public String test() {
        return TestService.printTest();
    }
```