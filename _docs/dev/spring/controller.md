---
title: controller
category: Springboot
order: 1
---

### controller
1.사용자의 요청이 진입하는 지점이며, 요청에 따라 어떤 처리를 할지 결정해주며 단, controller는 단지 결정만 해주고 실질적인 처리는 서비스에서 담당한다. 사용자에게 View를 응답으로 보낸다.

### controller를 쓰는 이유

대규모 서비스로 갈수록 처리해야하는 서비스가 많아지는데 이를 하나의 클래스에서 몰아 처리하고 중간 제어자 역할을 하는 것이다.
개발할 때보다 개발비용이나 유지보수비용이 대폭 줄어든다.

### controller 사용법
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

    @GetMapping(value = "testParam")
    public String testParam(@RequestParam int number) {

        return TestService.printNumber(number);
    }
```