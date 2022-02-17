<솔로몬접 사진 배너>



### 목차

------





### 🖌️ 솔로몬접 소개

------

- 개발 기간 : 2022. 01. 10 ~ 2022. 02. 18 (6 weeks)
- 개발 인원 : 이주용, 김도연, 김신아, 노건우, 황선주
- 주제 : 면접에 어려움을 겪고 있는 IT 취업준비생을 위한 화상 면접 서비스



### 👨‍👩‍👦 역할 및 팀원 소개

------

| Name     | 이주용                                         | 김도연                                 | 김신아                                       | 노건우                               | 황선주                                         |
| -------- | ---------------------------------------------- | -------------------------------------- | -------------------------------------------- | ------------------------------------ | ---------------------------------------------- |
| Profile  |                                                |                                        |                                              |                                      |                                                |
| Position | 팀장 & Frontend & UI/UX                        | Backend                                | Backend                                      | Frontend & UI/UX                     | Backend & WebRTC                               |
| Git      | @[leejuyong12](https://github.com/leejuyong12) | @[kid-owo](https://github.com/kid-owo) | @[dodssockii](https://github.com/dodssockii) | @[rogonu](https://github.com/rogonu) | @[hwangseonju](https://github.com/hwangseonju) |



### 핵심 기능

------







### 🛠️ 기술 스택

------

##### Back-End

##### <img src="https://img.shields.io/badge/java-8-007396?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/spring boot-2.4.0-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"><img src="https://img.shields.io/badge/JPA-6DB33F?style=for-the-badge&logo=Hibernate&logoColor=white"><img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=Gradle&logoColor=white"><img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> <img src="https://img.shields.io/badge/Openvidu-2.20.0-00d462?style=for-the-badge&logo=&logoColor=black">

##### <img src="https://img.shields.io/badge/Openvidu-2.20.0-ffcd00?style=for-the-badge&logo=&logoColor=black">

##### Front-End

<img src="https://img.shields.io/badge/vue.js-3.2.9-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> <img src="https://img.shields.io/badge/bootstrap-2.21.2-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white"> <img src="https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=HTML5&logoColor=white"> <img src="https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=CSS3&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black">

##### Tool

<img src="https://img.shields.io/badge/GitLab-FCA121?style=for-the-badge&logo=GitLab&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white"> <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=white"> <img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=JiraSoftware&logoColor=white"> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">

##### Architecture

<아키텍처 이미지>

<details>
<summary>Back-end 기술 스택 보기</summary>
<div markdown="1">

- Spring-Boot : 2.4.0
- Spring-Boot-Data-JPA
- Spring-Boot-Starter-JDBC
- Spring Security
- Spring-Boot-Starter-thymeleaf
- lombok
- mysql
- jjwt : 0.11.2
- Spring-Boot-Starter-Mail
- Swagger : 2.3.0 
- Openvidu-java-client : 2.20.0
- Openvidu-test-browsers : 1.0.0

</div>
</details>

<details>
<summary>Front-end 기술 스택 보기</summary>
<div markdown="1">

- JS
- HTML
- CSS
- Vue.js @3.2.29

라이브러리

- axios @0.25.0 : Promise 기반 HTTP 클라이언트
- bootstrap-vue @2.21.2
- Openvidu-bowser @2.20.0 : WebRTC 라이브러리
- eslint & prettier @6.7.2 : 협업을 위한 formatter 라이브러리

</div>
</details>



### ⚙️ 설정 및 실행

------

- 설치 환경

  -> AWS EC2 Linux, Docker, Docker-compose

<details>
    <summary>1. Java8 버전 설치</summary>
    <div>
- Azul public key 추가

  ```shell
  $sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0x219BD9C9
  ```

- Azul repository 추가

  ```shell
  $sudo apt-add-repository 'deb http://repos.azulsystems.com/ubuntu stable main'
  ```

- zulu-8 설치

  ```shell
  $sudo apt-get update
  $sudo apt-get install zulu-8
  ```

- 환경변수 설정

  ```shell
  $cd /etc
  $sudo nano profile
  ```

  본인의 환경에 맞게 설정

</details>



<details>
    <summary>2. Docker & Docker-compose 설치</summary>
    <div>

        - apt 패키기 인덱스 업데이트
    
      ```shell
      $sudo apt update && sudo apt upgrade
      ```
    
    - 다운로드를 위한 Util 준비
    
      ```shell
      $sudo apt-get install \
      apt-transport-https \
      ca-certificates \
      curl \
      gnupg-agent \
      software-properties-common
      ```
    
    - Docker GPG key 추가
    
      ```shell
      $curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add
      ```
    
    - apt repo에 Docker 다운로드 경로 추가
    
      ```shell
      $sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
      ```
    
    - Docker 다운로드 및 설치
    
      ```shell
      $sudo apt-cache policy docker-ce
      $sudo apt install docker-ce
      $sudo apt update
      ```
    
    - sudo 없이 docker 사용을 위한 ubuntu user docker 그룹에 등록 후 서버 재부팅
    
      ```shell
      $sudo usermod -aG docker ubuntu
      $sudo reboot
      ```
    
    - Ubuntu 계정 비밀번호 설정(없다면)
    
      ```shell
      $sudo passwd ubuntu
      ```
    
    - Docker-compose 설치
    
      ```shell
      $sudo curl -L https://github.com/docker/compose/releases/download/1.25.0-rc2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
      ```
    
    - 실행 권한 주기
    
      ```shell
      $sudo chmod +x /usr/local/bin/docker-compose
      ```
        
    </div>
</details>





2. Docker & Docker-compse 설치

- apt 패키기 인덱스 업데이트

  ```shell
  $sudo apt update && sudo apt upgrade
  ```

- 다운로드를 위한 Util 준비

  ```shell
  $sudo apt-get install \
  apt-transport-https \
  ca-certificates \
  curl \
  gnupg-agent \
  software-properties-common
  ```

- Docker GPG key 추가

  ```shell
  $curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add
  ```

- apt repo에 Docker 다운로드 경로 추가

  ```shell
  $sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
  ```

- Docker 다운로드 및 설치

  ```shell
  $sudo apt-cache policy docker-ce
  $sudo apt install docker-ce
  $sudo apt update
  ```

- sudo 없이 docker 사용을 위한 ubuntu user docker 그룹에 등록 후 서버 재부팅

  ```shell
  $sudo usermod -aG docker ubuntu
  $sudo reboot
  ```

- Ubuntu 계정 비밀번호 설정(없다면)

  ```shell
  $sudo passwd ubuntu
  ```

- Docker-compose 설치

  ```shell
  $sudo curl -L https://github.com/docker/compose/releases/download/1.25.0-rc2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
  ```

- 실행 권한 주기

  ```shell
  $sudo chmod +x /usr/local/bin/docker-compose
  ```

  

3. MySql  설치

- mysql server 설치

  ```shell
  $sudo apt update
  $sudo apt-get install mysql-server
  ```

- 대소문자 구별 default값 변경

  - msyql.cnf 파일에 ‘lower_case_table_names = 1’ 추가

  ```shell
  $sudo service mysql stop
  $sudo rm -rf /var/lib/mysql
  $sudo mkdir /var/lib/mysql
  $sudo chown mysql:mysql /var/lib/mysql
  $sudo chmod 700 /var/lib/mysql
  $cd /etc/mysql/mysql.conf.d
  $sudo nano mysqld.cnf
  ```

- mysql 서비스 재시작

  ```shell
  $sudo mysqld --defaults-file=/etc/mysql/my.cnf --initialize --lower_case_table_names=1 --user=mysql --console
  $sudo service mysql start
  ```

- 생성된 root의 비밀번호 검색

  ```shell
  $sudo grep 'temporary password' /var/log/mysql/error.log
  ```

- mysql 세션 접속해서 비밀번호 변경

  - 비밀번호를 변경해야 root 계정 접속 가능

  ```shell
  $sudo mysql -u root -p
  // password 입력
  > mysql : alter user 'root'@'localhost' identified by '새비밀번호 입력';
  ```

- 외부 접속 허용

  - 모든 IP 허용

    - mysql.cnf 파일에 ‘bind-address = 0.0.0.0’으로 수정하기 혹은 

      bind-address 주석처리하기 → 같은 결과

    ```shell
    $cd /etc/mysql/mysql.conf.d
    $sudo nano mysqld.cnf
    ```

  - 설정 적용을 위한 재시작

    ```shell
    $sudo service mysql restart
    ```

  - 사용자 계정 추가 

    - 사용자를 생성하고, 모든 권한(CRUD) 부여

    ```shell
    $sudo mysql -u root -p
    //password 입력
    > CREATE USER 'root'@'%' IDENTIFIED BY '새 비밀번호 입력';
    > GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;
    > FLUSH PRIVILEGES;
    ```

- Public IP 조회하기

  ```shell
  $curl ifconfig.me
  ```

  

4. Nginx 설치 및 세팅

- Nginx 설치 후 버전 확인

  ```shell
  $sudo apt install nginx
  $nginx -v
  ```

  

- 



5. Git repository clone

```shell
$git clone https://lab.ssafy.com/s06-webmobile1-sub2/S06P12C207.git
```



6. Openvidu Setting



1. Frontend

   

2. Backend



### 📜 Project ProgressStatus

------

| 구분      | 링크                                                         |
| --------- | ------------------------------------------------------------ |
| Notion    | [notion](https://feline-pluto-dd6.notion.site/393ec2193d8d4ec2976a198e5b00a699) |
| Documents | ppt 다운 링크                                                |
| WireFrame | link                                                         |
| UCC?      |                                                              |



#### :copyright: Copyright

------

