---
title: "How to setup the development environment for Angular on Windows 10"
categories: [Angular]
tags: [Angular, Node, Angular Application]
---

## How to setup the development environment for Angular on Windows 10

1. Install **Node**
* Visit Node.js web site (<https://nodejs.org/en/>).
* Download latest **‘LTS’** version.
![Node js web site](https://user-images.githubusercontent.com/32950391/80871339-fb1af200-8c79-11ea-9c92-df2d17cb07c9.jpg)
* Run **downloaded Installation file** ‘node-v12.16.3-x64.msi’
![downloaded Installation file](https://user-images.githubusercontent.com/32950391/80871586-716c2400-8c7b-11ea-94d6-67c8111df921.jpg)

2. Welcome to the Node.js Setup Wizard
* Click **‘Next’** button
![Welcome to the Node js Setup Wizard](https://user-images.githubusercontent.com/32950391/80871718-dde72300-8c7b-11ea-93a1-1a0fbb7cb523.jpg)

3. End-User License Agreement
* Check **‘I accept the terms in the License Agreement’** check box.
* Click **‘Next’** button
![End-User License Agreement](https://user-images.githubusercontent.com/32950391/80871824-1424a280-8c7c-11ea-8315-56a5babe4d2c.jpg)

4. Destination Folder
* Check the folder to install Node.js.
* Click **‘Next’** button
![Destination Folder](https://user-images.githubusercontent.com/32950391/80871872-741b4900-8c7c-11ea-845b-591f06786364.jpg)

5. Custom Setup
* Click **‘Next’** button
![Custom Setup](https://user-images.githubusercontent.com/32950391/80871929-b5135d80-8c7c-11ea-8819-ef2990bb54e1.jpg)

6. Tools for Native Modules
* Check **‘Automatically install the necessary tools. ...’** check box.
* Click **‘Next’** button
![Tools for Native Modules](https://user-images.githubusercontent.com/32950391/80871971-0a4f6f00-8c7d-11ea-8c89-6fa37e6f6893.jpg)

7. Ready to install Node.js
Click **‘Install’** button
![Ready to install Node js](https://user-images.githubusercontent.com/32950391/80872018-51d5fb00-8c7d-11ea-9168-f53d78fd57af.jpg)

8. Installing Node.js
![Installing Node js](https://user-images.githubusercontent.com/32950391/80872046-8d70c500-8c7d-11ea-8d6c-bc74b3fd8402.jpg)

9. **Completed** the Node.js Setup Wizard
* Click **‘Finish’** button.
![Completed the Node js Setup Wizard](https://user-images.githubusercontent.com/32950391/80872095-d4f75100-8c7d-11ea-9bdc-43dfe76ce8f2.jpg)

10. Install **Additional Tools** for Node.js
* Command Prompt runs
* Press **‘Enter’** key in the Command Prompt
![Install Additional Tools for Node js](https://user-images.githubusercontent.com/32950391/80872125-17b92900-8c7e-11ea-823d-c3138231e2c1.jpg)

11. Administrator: Windows PowerShell
* Windows PowerShell runs.
* Additional Tools are installed.
![Administrator Windows PowerShell](https://user-images.githubusercontent.com/32950391/80872184-52bb5c80-8c7e-11ea-859a-e2cc3e9fde60.jpg)
* After installing tools, press ‘Enter’ key in the Windows PowerShell.
![After installing tools](https://user-images.githubusercontent.com/32950391/80872215-89917280-8c7e-11ea-968d-dfd767707fb6.jpg)
* *Windows PowerShell window closes.

12. Check **NPM (Node Package Manager)** is installed.
* Run ‘Command Prompt’
* Enter **‘node -v’**. You can check the installed version of ‘Node’.
```
C:>node -v
v12.16.3
C:>
```
* Enter **‘npm -v’**. You can check the installed version of ‘NPM’
```
C:>npm -v
6.14.4
C:>
```

13. Install the **Angular CLI**
* Run ‘Command Prompt’
* Enter **‘npm install -g @angular/cli’**
```
C:\>npm install -g @angular/cli
```
![npm install -g @angular/cli](https://user-images.githubusercontent.com/32950391/80872399-aed2b080-8c7f-11ea-9b35-632c4e2c4b43.jpg)

14. Create a workspace and initial application
* Run ‘Command Prompt’
* Change to the directory that you want to make Angular application.
  - You can make directory if the directory does not exist.
```
C:\>mkdir angular_dir
C:\>cd angular_dir
C:\angular_dir>
```
* Enter ‘ng new my-angular-app’ in the command prompt.
  - ‘my-angular-app’ directory will be created.
```
C:\angular_dir>ng new my-angular-app
```
![ng new my-angular-app (1)](https://user-images.githubusercontent.com/32950391/80872566-b0e93f00-8c80-11ea-9bf5-4d89b36590c2.jpg)
![ng new my-angular-app (2)](https://user-images.githubusercontent.com/32950391/80872570-b5155c80-8c80-11ea-8e05-de6b54a82fca.jpg)
![ng new my-angular-app (3)](https://user-images.githubusercontent.com/32950391/80872575-b8104d00-8c80-11ea-92e4-37d94ce95496.jpg)

15. **Run** the Angular application
* Change directory to created directory
* Enter **‘cd my-angular-app’** in the command prompt.
```
C:\angular_dir>cd my-angular-app
C:\angular_dir\my-angular-app>
```
* Enter **‘ng serve --open’** in the command prompt.
```
C:\angular_dir\my-angular-app>ng serve --open
```
![ng serve --open](https://user-images.githubusercontent.com/32950391/80872781-302b4280-8c82-11ea-81fc-b95b789fe8f8.jpg)
* Then, you will see the **angular application** in the **web browser**.
![angular application in the web browser](https://user-images.githubusercontent.com/32950391/80872806-56e97900-8c82-11ea-8682-6866782c5fb4.jpg)










