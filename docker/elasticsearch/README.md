## INFORMATION

- single-node

## INITIAL SETTINGS

1. root 유저가 아닌 경우, 미리 폴더를 생성해야 함
```
mkdir -p elasticsearch/data/es01
```

2. .env_template 양식에 맞춰 .env 파일을 생성한다.

```
VERSION=7.17.0 or VERSION=7.17.0-arm64
```

## Filebeat 사용법

container를 지정하려면 docker ps로 컨테이너 ID 확인 후

inputs의 paths를 '... containers/[CONTAINER ID]*/*.log'로 변경

### filebeat - processor

index_search_slowlog 로그만 수집하기 위해 나머지 이벤트는 버리는 방식