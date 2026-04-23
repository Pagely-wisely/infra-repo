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