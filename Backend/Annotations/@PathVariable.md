## @PathVariable 경로변수

PathVariable를 사용하여 리소스 경로에 식별자를 넣어서 동적으로 URL에 정보를담을수있음

```java
@PatchMapping("/update/{id}")
    public ResponseEntity<Void> updateNotice(@PathVariable Long id, @Valid @RequestBody NoticeUpdateRequest request) {
        noticeUserUpdateService.updateNotice(id, request);
        return ResponseEntity.ok().build();
    }
    //위는 우리 푸딩 코드에서 @pathvariable를 사용한 예시이다
```

URL의**{Id}와** 매개변수 **long Id**와 **이름을 맞춰준다.**

**여러 개의** PathVariable을 동시에 사용할 수 있다.