
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
 - Standard-IA : 비용효율적인 저장 솔루션 (엑세스 빈도가 낮은 파일 처리에 효율적)
 - Standard : 페타바이트 규모의 데이터 저장 가능
 
#### Storage Gateway 파일 게이트웨이
 - 온프로미스와 AWS 스토리지 연결
 - iSCSi  가상 테이프 라이브러리 (VTL) : 백업 어플리케이션 연결

#### AWS DataSync
 - 데이터 온라인 마이그레이션 솔루션 : 온프로미스 nfs 서버에서 s3 버킷으로 마이그레이션 처리

#### Snowball 엣지 스토리지
 - 오프라인 마이그레이션 솔루션

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

#### Elastic Beanstalk
 - 다중 AZ 로드 발란싱

#### ACM
 - HTTPS 인증서

#### CloudFront
 - 배포생성 및 가격 등급 선택

#### VCP
 - VPC 엔드포인트 : 데이터 출력 비용을 줄일수 있습니다.
 - S3서비스를 프라이빗하게 연결할 수 있습니다.
 - 라우팅 테이블 구성에 따라 인터넷 엑세스 가능

#### AMI 
 - EC2 인스턴스 복사 및 다른 리전 지정이 가능합니다.

#### Auto Scaling
 - 대상 추적 조정 정책 : cpu 사용률에 따라 Auto Scaling 그룹을 조정합니다.
 - 예정된 스케일링을 사용하여 최소, 최대 용량을 0 으로 변경하면 인스턴스가 작동하지 않습니다.

#### 온디맨드
 - 단기 인스턴스 사용에 적합

#### CloudWath
 - 머신러닝을 사용하여 올바른 스케일링 정책 데이터기반의 용량 필요량을 예측할수 있습니다.
