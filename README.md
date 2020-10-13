# Linux_systemclt
리눅스 서비스 시스템 등록 방법


# .service 파일 생성
>> CentOS 기반 
/usr/lib/systemd/system
경로에 예제를 참고한 .service 파일 생성

*파일 생성시 type 꼭 지정
type = fork     // 데몬처럼 실행 되는 서비스 , 백그라운드로 실행되는 서비스
type = simple(Default)   // 백그라운도로 실행 되지 않는 것들(return 되는 것들)


# 자동 실행 서비스 등록
systemctl enable xxx.service

# 서비스 실행
systemctl start xxx.service 

# 서비스 중지
systemctl stop xxx.service

# 서비스 상태 확인
systemctl status xxx.service

# 서비스 목록 확인
systemctl list-units --type=service

# 서비스 자동 실행 유무 확인
systemctl is-enabled xxx.service

