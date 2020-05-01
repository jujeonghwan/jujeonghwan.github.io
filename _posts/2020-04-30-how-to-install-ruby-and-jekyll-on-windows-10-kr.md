---
title:  "윈도우10에 Ruby와 Jekyll을 설치하는 방법"
categories: [Jekyll]
tags: [Ruby, Jekyll]
---

## 윈도우10에 Ruby와 Jekyll을 설치하는 방법

1. RubyInstaller 웹 사이트 (<https://rubyinstaller.org>)를 방문하십시오.

2. 웹 페이지에서 **‘Download’** 버튼을 클릭하십시오.
![RubyInstaller web site](https://user-images.githubusercontent.com/32950391/80770403-37d1d680-8b1e-11ea-8035-05227f3d767d.JPG)

3. RubyInstaller 다운로드 웹 페이지 (<https://rubyinstaller.org/downloads/>)에서,
* **‘Ruby+Devkit 2.6.6-1 (x64)’** 링크를 클릭하고 파일을 로컬 폴더 (예: ‘다운로드’)에 저장하십시오.
![Ruby Installer Downloads Page](https://user-images.githubusercontent.com/32950391/80771827-a4e76b00-8b22-11ea-8566-88e7648c5f0b.JPG)
![Ruby Installer file Save As](https://user-images.githubusercontent.com/32950391/80771931-eaa43380-8b22-11ea-9656-314f9558d2e9.JPG)

4. 다운로드가 완료된 후, **설치 파일** (rubyinstaller-devkit-2.6.6-1-x64.exe)을 더블클릭 하십시오.
![Ruby Installer file folder](https://user-images.githubusercontent.com/32950391/80772068-69996c00-8b23-11ea-97f2-a89e7cfa0845.JPG)

5. Setup – Ruby 2.6.6-1-x64 with MSYS2.
* Ruby 2.6.6-1-x64 with MSYS2 License Agreement.
  - **‘I accept the License’** 옵션을 선택하십시오.
  - **‘Next’** 버튼을 클릭하십시오.
![Ruby with MSYS2 License Agreement](https://user-images.githubusercontent.com/32950391/80772206-ee848580-8b23-11ea-8fd6-d6b93f8ec882.JPG)

6. Installation Destination and Optional Tasks
* 설치할 폴더에 ‘C:\Ruby26-x64’를 입력하고 **3가지 옵션** (‘Add Ruby executables to your PATH’, ‘Associate .rb and .rbw files with this Ruby installation’, ‘Use UTF-8 as default external encoding’)을 모두 체크하십시오.
* **‘Install’** 버튼을 클릭하십시오.
![Installation Destination and Optional Tasks](https://user-images.githubusercontent.com/32950391/80772460-dc571700-8b24-11ea-8217-66f90562b516.JPG)

7. Select Components
* ‘Development Kit’를 설치하려면 **‘MSYS2 development toolchain 2020-04-03’** 옵션을 체크하십시오.
* **‘Next’** 버튼을 클릭하십시오.
![Select Components](https://user-images.githubusercontent.com/32950391/80772567-2cce7480-8b25-11ea-9799-582d802f0e22.JPG)
![Installing Components](https://user-images.githubusercontent.com/32950391/80772632-5d161300-8b25-11ea-968d-068e4a9efce2.JPG)

8. Completing the Ruby 2.6.6-1-x64 with MSYS2 Setup Wizard
* ‘Ruby’ 설치완료 내용을 확인한 후 **‘Finish’** 버튼을 클릭하십시오.
![Completing the Ruby](https://user-images.githubusercontent.com/32950391/80772697-99497380-8b25-11ea-9fd3-641425ddb872.JPG)

9. Command Prompt
* **‘명령 프롬프트’** 창이 실행된다.
* 명령 프롬프트에서 **‘Enter’**키를 누르십시오.
  - 예. Which components shall be installed? If unsure press ENTER [1,3] 
![Command Prompt window](https://user-images.githubusercontent.com/32950391/80772872-212f7d80-8b26-11ea-9932-a1b06f99fd04.JPG)
* 명령 프롬프트에서 **‘Enter’**키를 누르십시오.
  - 예. Which components shall be installed? If unsure press ENTER [] 
  - 그러면, ‘명령 프롬프트’ 창이 닫힌다.
![Ruby Installer 2 for Windows](https://user-images.githubusercontent.com/32950391/80772971-7b304300-8b26-11ea-9dae-dfac93184465.JPG)

10. Ruby가 제대로 설치되었는지 확인하십시오.
* **‘명령 프롬프트’**를 실행하십시오.
![Run ‘Command Prompt’](https://user-images.githubusercontent.com/32950391/80773057-b5014980-8b26-11ea-810c-2817f10334dc.JPG)

11. 명령 프롬프트에서 **‘ruby -v’**를 입력하십시오.
* 설치된 ‘Ruby’의 **버전**을 확인할 수 있습니다.
![installed version of ‘Ruby’](https://user-images.githubusercontent.com/32950391/80773273-63a58a00-8b27-11ea-8d6e-272984883245.JPG)
* 명령 프롬프트에서 **‘irb’**를 입력하십시오.
* IRB (Interactive Ruby)를 실행할 수 있습니다.
* IRB 프롬프트에서 **‘exit()’**를 입력하십시오.
* IRB를 종료할 수 있습니다.
![‘irb’ and 'exit()' in the command prompt](https://user-images.githubusercontent.com/32950391/80773508-1d045f80-8b28-11ea-872a-8c0255657a00.JPG)

12. Jekyll을 설치하십시오.
* **‘명령 프롬프트’**를 실행하십시오.
* 명령 프롬프트에서 **‘gem -v’**를 입력하십시오.
  - 설치된 **‘gem’의 버전**을 확인할 수 있습니다. – RubyGems는 루비 프로그래밍 언어를 위한 패키지 매니저입니다.
![‘gem -v’ in the command prompt](https://user-images.githubusercontent.com/32950391/80774416-f562c680-8b2a-11ea-9da2-a93ced9f2d25.JPG)
* 명령 프롬프트에서 **‘gem install jekyll bundler’**를 입력하십시오.
![‘gem install jekyll bundler’ in the command prompt](https://user-images.githubusercontent.com/32950391/80774527-48d51480-8b2b-11ea-951f-72a715941302.JPG)
* 명령 프롬프트에서 **‘jekyll -v’**를 입력하십시오.
  - 설치된 **‘jekyll’의 버전**을 확인할 수 있습니다.
![‘jekyll -v’ in the command prompt](https://user-images.githubusercontent.com/32950391/80774615-8174ee00-8b2b-11ea-9105-68951ae5b40f.JPG)
