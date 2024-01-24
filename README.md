# AWS 

## AWS를 사용하는 세 가지 방법
1. AWS 콘솔
2. AWS CLI
3. AWS SDK 라이브러리
```
1번과 2번 AWS 콘솔과 CLI를 사용한다.
```
## AWS 계정 생성
[AWS 계정생성](https://portal.aws.amazon.com/billing/signup#/start)
![image](https://github.com/mr-won/AWS/assets/58906858/a18cc673-fd81-44f1-a861-0b3ed60667b3)
```
컴퓨터공학과 학부 수업 때 생성해두었던 AWS 계정이 있어서 이것을 사용하기로 한다.
```
## 파이썬 설치
[파이썬3 설치](https://www.python.org/downloads/windows/)
![image](https://github.com/mr-won/AWS/assets/58906858/1d7449ee-279f-40a7-969e-33517d3a0b64)
```
AWS CLI와 EB CLI는 파이썬 기반으로 작동한다. 따라서 파이썬 3을 설치한다.
```
## AWS CLI 설치
[AWS CLI 설치](https://awscli.amazonaws.com/AWSCLIV2.msi)
![image](https://github.com/mr-won/AWS/assets/58906858/36071523-0a4b-44c1-ae31-b686888be825)

## AWS CLI 설정
![image](https://github.com/mr-won/AWS/assets/58906858/cfde390f-895f-44b7-b25f-31d01e1a147a)
```
AWS 콘솔에 로그인한 후 IAM으로 들어간다.
```
![image](https://github.com/mr-won/AWS/assets/58906858/e528747d-a9fd-473f-8892-28358df0d5a3)
```
IAM에서 사용자 추가를 클릭하여 프로그래밍 방식 엑세스로 사용자를 추가한다.
```
1. 프로그래밍 방식 : 액세스 키와 시크릿 키가 자동으로 생성
2. AWS Management Console 엑세스 : 아이디와 비밀번호를 지정하는 로그인 유저가 되는 것
![image](https://github.com/mr-won/AWS/assets/58906858/75e3cf23-e69a-4637-b51f-6878034d10e1)
```
기존 정책 집적 연결을 누른 후 AdministratorAcess를 선택한다.
```
AdministratorAccess : 모든 AWS 리소스(EC22, RDS, EMR, 등등)에 대해 모든 권한을 준다.   
![image](https://github.com/mr-won/AWS/assets/58906858/9c305f8b-b3f4-4908-94d4-aa5c50f66049)
```
IAM 사용자를 생성한 후 엑세스 키를 AWS CLI 사용 목적으로 생성한다.
엑세스 키와 비밀 엑세스 키를 반드시 따로 메모한다. 나는 .CSV파일로 다운하였다.
```
## AWS Credential 설정
![image](https://github.com/mr-won/AWS/assets/58906858/368ff582-f764-46d3-80c3-b49ee1fe158a)
```cmd
$ aws configure
AWS Access Key ID [None] : <액세스 키 ID>
AWS Secret Access Key [None] : <비밀 액세스 키>
Default region name [None] : ap-northeast-2
Default output format [None] : json
```
Default region name : AWS 데이터 센터가 있는 장소의 이름을 뜻하는 데 서비스를 실제로 사용할 사용자와        
서비스가 호스팅되고 있는 데이터 센터가 가까울수록 네트워크 대기 시간이 짧아진다.    
한국에 사용자가 거주할 확률이 높아서 ap-northeast-2를 선택하였다.   






