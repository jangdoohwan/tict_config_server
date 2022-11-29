Spring Cloud Config Server
===


목차
---
1. [버전정보](#버전정보)
2. [실행]($#실행)

---

## 버전정보

- spring boot 2.7.4
- gradle 7.5


## 실행
curl http://localhost:8080/coll/local/tict
http://{서버주소}/{어플명}/{프로파일명}/{브런치명}

### 필수 환경변수

- spring.profiles.active

on terminal
```
java -Dspring.profiles.active=git -Dspring.cloud.config.server.git.uri=http://slc.conv.site:13203/tict/config-repository.git -Dspring.cloud.config.server.git.username=dhj -Dspring.cloud.config.server.git.password=XehbyozVResWdvhZyhdh -jar config.jar

```


on Intellij Community
- Run/Debug Configurations > bootRun 선택 > Modify options > select add VM options > VM options 입력
```
-Dspring.profiles.active=git -Dspring.cloud.config.server.git.uri=http://slc.conv.site:13203/tict/config-repository.git -Dspring.cloud.config.server.git.username=dhj -Dspring.cloud.config.server.git.password=XehbyozVResWdvhZyhdh
```