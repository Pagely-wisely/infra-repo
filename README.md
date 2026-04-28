# infra-rep
Pagely 서비스의 공용 인프라 환경(PostgreSQL, Redis, Config Server, Eureka, Gateway 등)과 로컬/배포용 인프라 설정을 관리하는 레포


---

### 서비스 별 각 env 세팅 방법

```
cd ~/pagely/meeting-service
set -a
source .env
set +a
./gradlew bootRun
```

### kafka, kafka-ui 실행 방법

- kafka-ui 는 배포 환경에서는 필요하지않을 수 있어, profile `ui` 활성화 시에만 실행되도록 설정했습니다.

```
## kafka 단독 실행
docker compose -f docker-compose.kafka.yaml up -d

## kafka-ui 같이 실행
docker compose -f docker-compose.kafka.yaml --profile ui up -d

## 종료
docker compose -f docker-compose.kafka.yaml down
```
