---
title: "윈도우10에 Angular 개발환경을 설치하는 방법"
categories: [Angular]
tags: [Angular, Node, Angular Application]
---

## 윈도우10에 Angular 개발환경을 설치하는 방법

1. **Node** 설치
* Node.js 웹 사이트 (<https://nodejs.org/en/>)를 방문하십시오.
* 최신 **‘LTS’** 버전 Node 설치파일을 다운로드 받으십시오.
![Node js web site](https://user-images.githubusercontent.com/32950391/80871339-fb1af200-8c79-11ea-9c92-df2d17cb07c9.jpg)
* 다운로드한 **설치파일** (예. node-v12.16.3-x64.msi’)을 실행하십시오.
![downloaded Installation file](https://user-images.githubusercontent.com/32950391/80871586-716c2400-8c7b-11ea-94d6-67c8111df921.jpg)

2. Welcome to the Node.js Setup Wizard
* **‘Next’** 버튼을 클릭하십시오.
![Welcome to the Node js Setup Wizard](https://user-images.githubusercontent.com/32950391/80871718-dde72300-8c7b-11ea-93a1-1a0fbb7cb523.jpg)

3. End-User License Agreement
* **‘I accept the terms in the License Agreement’** 체크박스를 체크하십시오.
* **‘Next’** 버튼을 클릭하십시오.
![End-User License Agreement](https://user-images.githubusercontent.com/32950391/80871824-1424a280-8c7c-11ea-8315-56a5babe4d2c.jpg)

4. Destination Folder
* Node.js를 설치할 폴더를 확인하십시오.
* **‘Next’** 버튼을 클릭하십시오.
![Destination Folder](https://user-images.githubusercontent.com/32950391/80871872-741b4900-8c7c-11ea-845b-591f06786364.jpg)

5. Custom Setup
* **‘Next’** 버튼을 클릭하십시오.
![Custom Setup](https://user-images.githubusercontent.com/32950391/80871929-b5135d80-8c7c-11ea-8819-ef2990bb54e1.jpg)

6. Tools for Native Modules
* **‘Automatically install the necessary tools. ...’** 체크박스를 체크하십시오.
* **‘Next’** 버튼을 클릭하십시오.
![Tools for Native Modules](https://user-images.githubusercontent.com/32950391/80871971-0a4f6f00-8c7d-11ea-8c89-6fa37e6f6893.jpg)

7. Ready to install Node.js
* **‘Install’** 버튼을 클릭하십시오.
![Ready to install Node js](https://user-images.githubusercontent.com/32950391/80872018-51d5fb00-8c7d-11ea-9168-f53d78fd57af.jpg)

8. Installing Node.js
![Installing Node js](https://user-images.githubusercontent.com/32950391/80872046-8d70c500-8c7d-11ea-8d6c-bc74b3fd8402.jpg)

9. **Completed** the Node.js Setup Wizard
* **‘Finish’** 버튼을 클릭하십시오.
![Completed the Node js Setup Wizard](https://user-images.githubusercontent.com/32950391/80872095-d4f75100-8c7d-11ea-9bdc-43dfe76ce8f2.jpg)

10. Install **Additional Tools** for Node.js
* **‘명령 프롬프트’** 창이 실행된다.
* 명령 프롬프트에서 **‘Enter’**키를 누르십시오.
![Install Additional Tools for Node js](https://user-images.githubusercontent.com/32950391/80872125-17b92900-8c7e-11ea-823d-c3138231e2c1.jpg)

11. Administrator: Windows PowerShell
* **‘윈도우 파워셸’** 창이 실행된다.
* 추가 도구들이 설치된다.
![Administrator Windows PowerShell](https://user-images.githubusercontent.com/32950391/80872184-52bb5c80-8c7e-11ea-859a-e2cc3e9fde60.jpg)
* After installing tools, press ‘Enter’ key in the Windows PowerShell.
![After installing tools](https://user-images.githubusercontent.com/32950391/80872215-89917280-8c7e-11ea-968d-dfd767707fb6.jpg)
* *Windows PowerShell window closes.

12. **NPM (Node Package Manager)**가 제대로 설치되었는지 확인하십시오.
* **‘명령 프롬프트’**를 실행하십시오.
* 명령 프롬프트에서 **‘node -v’**를 입력하십시오. 설치된 ‘Node’의 **version**을 확인할 수 있습니다.
```
C:>node -v
v12.16.3
C:>
```
* 명령 프롬프트에서 **‘npm -v’**를 입력하십시오. 설치된 ‘NPM’의 **version**을 확인할 수 있습니다.
```
C:>npm -v
6.14.4
C:>
```

13. **Angular CLI**를 설치하십시오.
* **‘명령 프롬프트’**를 실행하십시오.
* 명령 프롬프트에서 **‘npm install -g @angular/cli’**를 입력하십시오.
```
C:\>npm install -g @angular/cli
```
![npm install -g @angular/cli](https://user-images.githubusercontent.com/32950391/80872399-aed2b080-8c7f-11ea-9b35-632c4e2c4b43.jpg)

14. 작업폴더와 초기 앱을 생성하십시오.
* **‘명령 프롬프트’**를 실행하십시오.
* Angular 앱을 만들길 원하는 **디렉터리**로 이동하십시오.
* 디렉터리가 존재하지 않는다면, 디렉터리를 만들 수 있습니다.
```
C:\>mkdir angular_dir
C:\>cd angular_dir
C:\angular_dir>
```
* 명령 프롬프트에서 **‘ng new my-angular-app’**를 입력하십시오.
  - 'my-angular-app'**디렉터리**는 생성될 것입니다.
```
C:\angular_dir>ng new my-angular-app
```
![ng new my-angular-app (1)](https://user-images.githubusercontent.com/32950391/80872566-b0e93f00-8c80-11ea-9bf5-4d89b36590c2.jpg)
![ng new my-angular-app (2)](https://user-images.githubusercontent.com/32950391/80872570-b5155c80-8c80-11ea-8e05-de6b54a82fca.jpg)
![ng new my-angular-app (3)](https://user-images.githubusercontent.com/32950391/80872575-b8104d00-8c80-11ea-92e4-37d94ce95496.jpg)

15. Angular 앱을 실행하십시도.
* 생성된 디렉터리로 이동합니다.
* 명령 프롬프트에서 **‘cd my-angular-app’**를 입력하십시오.
```
C:\angular_dir>cd my-angular-app
C:\angular_dir\my-angular-app>
```
* 명령 프롬프트에서 **‘ng serve --open’**를 입력하십시오.
```
C:\angular_dir\my-angular-app>ng serve --open
```
![ng serve --open](https://user-images.githubusercontent.com/32950391/80872781-302b4280-8c82-11ea-81fc-b95b789fe8f8.jpg)
* 그러면, 웹브라우저에서 **Angular 앱**을 볼 수 있습니다.
![angular application in the web browser](https://user-images.githubusercontent.com/32950391/80872806-56e97900-8c82-11ea-8682-6866782c5fb4.jpg)










