# 도커에서 서버 배포 쉽게 하려고 만든 도커 써-버
## 코드 바로 실행하기
```bash
wget https://raw.githubusercontent.com/FlanketITCoop/docker-server/master/install.sh && sh install.sh
```

## PMA 다운로드 및 설치
```bash
cd ./sources/default/
apt -y install unzip
wget https://files.phpmyadmin.net/phpMyAdmin/5.0.4/phpMyAdmin-5.0.4-all-languages.zip
unzip phpMyAdmin-5.0.4-all-languages.zip
mv phpMyAdmin-5.0.4-all-languages pma
```

## 폴더 설명
1. configure - Docker 빌드업 소스 경로
2. settings - 각종 환경설정파일 경로(아파치, PHP, 기타...)
    1. apache - 아파치 설정파일 경로
    2. php - php 설정파일 경로
    3. vhosts - 아파치 가상호스트 설정파일 경로
3. sources - 작업하면 되는 폴더
    1. mariadb - mariadb 데이터베이스가 저장되는 공간
    2. web - 웹 파일이 저장되는 공간
    3. default - 기본 경로 (도메인 연결 안 되었을때 표시 될 곳)
