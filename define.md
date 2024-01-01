
#### Amazon Redshift 클러스터
 - 데이터웨어하우스 솔루션

#### Amazon EMR 클러스터
 - ERM은 빅데이터 처리 솔루션

#### Elastic File System(Amazon EFS)
 - 여러 가용영역의 EC2 인스턴스에서 동시 연결 가능한 파일 스토리지 솔루션

#### IAM
 - 암호 만료 기간 설정에 따른 사용자 처리
 - 권한 경계 설정 : 관리자 정책 연결을 명시적으로 거부할 경우
 - 신뢰 정책 : dev -> prod 계정위임 처리

#### DynamDB
 - 트래픽 양에 따라 확장
 - 지정 시간복구 (point-in-time recovery) 구성
 - RPO 복구의 경우 원하는 시점으로 복원
 - 높은 읽기 처리량지원, 서버리스 서비스로 운영 오버헤드 최소화 하는 DB
 - 마이크로 초 단위 응답시간 제공, 개발 및 운영오버헤드 최소화

#### Amazon ElastiCache
 - 가장낮은 대기 시간 제공
 - 연결을 끊었다가 다시 연결해도 세션 데이터 유지

#### KMS (SSE-KMS)
 - 키를 매년 자동 순환 시키는 옵션
 - AWS가 마스터키 관리, 사용자가 데이터키 관리, 자동 키관리 및 교체, 키에 엑세스할 수 있는 사람 제어
 - 

#### NLB (Network Load Balacner)
 - 고정 IP 제공
 - TCP 트래픽 처리
  - 가용성 및 확장성 제공

#### ALB (Application Load Balancer)
 - HTTP 트래픽 처리 

#### S3
 - Transfer Acceleration : 전송 가속화 솔루션 (비용증가)
 - 불완전한 멀티파트 업로드를 삭제하는 S3 수명 주기 정책 활성화 (비용감소)
 - Intelligent-Tiering 스토리지 사용 : 수명주기 설정
 - Standard :
   - 페타바이트 규모의 데이터 저장 가능
   - 즉시검색 기능
   - 최소 과금 기간없음
- Standard-IA : 비용효율적인 저장 솔루션 (엑세스 빈도가 낮은 파일 처리에 효율적)
   - 최소 과금 기간 30일
 - Glacier
   - 신속검색 1-5분, 표준 3-5시간의 검색 시간소요
   - 최소 과금 기간 90일
 - Glacier Deppe Archive
   - 최소 과금 기간 180일

### Athena
 - 온디맨드 보고서 및 쿼리 실행 ( S3의 데이터를 쿼리할 수있는 서비스)
   
 
#### Storage Gateway 파일 게이트웨이
 - 온프로미스와 AWS 스토리지 연결
 - iSCSi  가상 테이프 라이브러리 (VTL) : 백업 어플리케이션 연결

#### AWS DataSync
 - 데이터 온라인 마이그레이션 솔루션 : 온프로미스 nfs 서버에서 s3 버킷으로 마이그레이션 처리

#### Snowball 엣지 스토리지
 - 오프라인 마이그레이션 솔루션

#### kinesis Data Analytics
 - 실시간 스트리밍 처리 솔루션

#### Kinesis Data Firehose
 - privateLink 를 사용하여 VPC에서 Kinesis Data Firehose용 인터페이스 VPC 엔드포인트 생성
 - 온프로미스 네트워크와 AWS 간 1Gbps AWS Direct Connect 연결 설정
 - PrivateLink 엔드포인트를 사용하여 온프로미스에서 Kinesis Data Firehose로 데이터 전송

#### SQS (Simple Queue Service)
 - 대기열 프로비저닝 (
 - 대기열 폴링 ec2 인스턴스 구성
 - 인스턴스 당 백로그 계산을 기반으로 메트릭 생성, 메트릭을 기반으로 AutoScailng 그룹을 확장합니다.

#### FSx (Windows 기반 파일시스템)
 - Windows 인스턴스 내 파일 시스템 공유
 - 고성능 컴퓨팅(HPC) 환경에 Lustre 영구(지속적) 파일 시스템 사용 가능

#### Elastic Beanstalk
 - 다중 AZ 로드 발란싱

#### ACM
 - HTTPS 인증서

#### CloudFront
 - 배포생성 및 가격 등급 선택
 - 요청 증가 시 엣지로케이션에 콘텐츠 캐싱으로 트래픽 분산

#### VCP
 - VPC 엔드포인트 : 데이터 출력 비용을 줄일수 있습니다.
 - S3서비스를 프라이빗하게 연결할 수 있습니다. (인터넷을 통과하지 않아도됨)
 - 라우팅 테이블 구성에 따라 인터넷 엑세스 가능

#### AMI 
 - EC2 인스턴스 복사 및 다른 리전 지정이 가능합니다.

#### Auto Scaling
 - 대상 추적 조정 정책 : cpu 사용률에 따라 Auto Scaling 그룹을 조정합니다.
 - 예정된 스케일링을 사용하여 최소, 최대 용량을 0 으로 변경하면 인스턴스가 작동하지 않습니다.
 - 예측 조정 활성화 : 머신러닝을 사용하여 CloudWath의 기록 데이터를 기반으로 필요량을 예측

#### 온디맨드
 - 단기 인스턴스 사용에 적합

#### CloudWath
 - 머신러닝을 사용하여 올바른 스케일링 정책 데이터기반의 용량 필요량을 예측할수 있습니다.

#### 클러스터 배치 그룹 (확인)
 - 서버를 고속 네트워크로 연결로 그룹화하여 네티워크 처리량 최대화

#### 전용 호스트
 - 하드웨어를 공유하지 않음

#### NAT 게이트웨이 (확인)
 - 많은 트래픽 지원 및  고가용성, 내결함성, 자동 확정성을 충족합니다.

#### AWS Fargate
 - 가용성이 높고 수요 증가에 맞게 확장 가능

#### Global Accelerator
 - 2개의 고정 IP를 가짐
 - 글로벌 사용자에게 최적화된 경로 제공으로 라우팅 속도를 빠르게 해줍니다.

#### Secrets Manager
 - 자격증명 자동 교체 가능, 자격증명 관리 서비스

#### Direct Connect
 - 온프로미스와 AWS 전용선 연결
 - 암호화 되지 않은 채널 전송 방법

#### Aurora
 - 복제본 추가 시 트래픽이 분산되어 요청속도가 빨라집니다.
 - 단일 DB 인스턴스로 구성되어도 데이터는 여러 가용영역에 복제 및 분산 저정 됨
 - 글로벌 데이터베이스 클러스터 : 다른 리전으로 데이터베이스를 복제하는 기능

#### VPN
 - 암호화된 채널 전송
 - 1Gbps 인터넷으로 10TB 전송에 20시간 소요

#### Inspector
 - EC2 및 컨테이너 워크로드 소프트웨어 취약점 관리 서비스

#### WAF
 - DDoS 공격 방어 가능
 - 특정 국가에서만 엑세스 제한 가능

#### ACL
 - 네트워크레벨 방화벽

#### GuardDuty
 - 지능형 위협 탐지 서비스

#### Cognito
 - 애플리케이션에 대한 로그인 및 인증 제공 기능

#### SAML (Security Assertion Markup Language) 2.0 기반 페데레이션
 - 온프로미스 AD 사용자를 AWS 액세스와 통합

