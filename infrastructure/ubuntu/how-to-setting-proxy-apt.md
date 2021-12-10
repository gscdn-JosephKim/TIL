# 내용
 - ubuntu 패키지 설치 관련 proxy 설정 방법
 - apt update 등을 수행할 때 외부 squid 등을 사용하려고 할 때 방법

# 설정

```bash
$ cat >> /etc/apt/apt.conf.d/80proxy.conf
Acquire {
  HTTP::proxy "http://10.178.0.2:80";
  HTTPS::proxy "http://10.178.0.2:80";
}
```
