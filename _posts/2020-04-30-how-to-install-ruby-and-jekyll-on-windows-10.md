---
title:  "How to install Ruby and Jekyll on Windows 10"
categories: [Jekyll]
tags: [Ruby, Jekyll]
---

## How to install Ruby and Jekyll on Windows 10

1. Visit **RubyInstaller** web site (<https://rubyinstaller.org/>).

2. Click the **‘Download’** button on the web page.
![RubyInstaller web site](https://user-images.githubusercontent.com/32950391/80770403-37d1d680-8b1e-11ea-8035-05227f3d767d.JPG)

3. On the RubyInstaller Downloads web page (<https://rubyinstaller.org/downloads/>),
* click the **‘Ruby+Devkit 2.6.6-1 (x64)’** link and save the file to the local folder (i.e. ‘Downloads’).
![Ruby Installer Downloads Page](https://user-images.githubusercontent.com/32950391/80771827-a4e76b00-8b22-11ea-8566-88e7648c5f0b.JPG)
![Ruby Installer file Save As](https://user-images.githubusercontent.com/32950391/80771931-eaa43380-8b22-11ea-9656-314f9558d2e9.JPG)

4. After the download is complete, double-click the **installation file** (rubyinstaller-devkit-2.6.6-1-x64.exe).
![Ruby Installer file folder](https://user-images.githubusercontent.com/32950391/80772068-69996c00-8b23-11ea-97f2-a89e7cfa0845.JPG)

5. Setup – Ruby 2.6.6-1-x64 with MSYS2.
* Ruby 2.6.6-1-x64 with MSYS2 License Agreement.
  - Select **‘I accept the License’** option.
  - Click the **‘Next’** button.
![Ruby with MSYS2 License Agreement](https://user-images.githubusercontent.com/32950391/80772206-ee848580-8b23-11ea-8fd6-d6b93f8ec882.JPG)

6. Installation Destination and Optional Tasks
* Input install folder ‘C:\Ruby26-x64’ into the ‘Installation Destination folder’ and check **all 3 options** (‘Add Ruby executables to your PATH’, ‘Associate .rb and .rbw files with this Ruby installation’, ‘Use UTF-8 as default external encoding’). 
* Click the **‘Install’** button.
![Installation Destination and Optional Tasks](https://user-images.githubusercontent.com/32950391/80772460-dc571700-8b24-11ea-8217-66f90562b516.JPG)

7. Select Components
* Check **‘MSYS2 development toolchain 2020-04-03’** option if you want to install ‘Development Kit’.
* Click the **‘Next’** button.
![Select Components](https://user-images.githubusercontent.com/32950391/80772567-2cce7480-8b25-11ea-9799-582d802f0e22.JPG)
![Installing Components](https://user-images.githubusercontent.com/32950391/80772632-5d161300-8b25-11ea-968d-068e4a9efce2.JPG)

8. Completing the Ruby 2.6.6-1-x64 with MSYS2 Setup Wizard
* After confirming that the Ruby is installed, click the **‘Finish’** button.
![Completing the Ruby](https://user-images.githubusercontent.com/32950391/80772697-99497380-8b25-11ea-9fd3-641425ddb872.JPG)

9. Command Prompt
* **‘Command Prompt’** window runs.
* Press the **‘Enter’** key in the Command Prompt.
  - i.e. Which components shall be installed? If unsure press ENTER [1,3] 
![Command Prompt window](https://user-images.githubusercontent.com/32950391/80772872-212f7d80-8b26-11ea-9932-a1b06f99fd04.JPG)
* Press the **‘Enter’** key in the Command Prompt.
  - i.e. Which components shall be installed? If unsure press ENTER [] 
  - Then, ‘Command Prompt’ window closes.
![Ruby Installer 2 for Windows](https://user-images.githubusercontent.com/32950391/80772971-7b304300-8b26-11ea-9dae-dfac93184465.JPG)

10. Check that the Ruby is properly installed.
*	Run **‘Command Prompt’**
![Run ‘Command Prompt’](https://user-images.githubusercontent.com/32950391/80773057-b5014980-8b26-11ea-810c-2817f10334dc.JPG)

11. Enter **‘ruby -v’** in the command prompt.
* You can check the installed **version** of ‘Ruby’.
![installed version of ‘Ruby’](https://user-images.githubusercontent.com/32950391/80773273-63a58a00-8b27-11ea-8d6e-272984883245.JPG)
* Enter **‘irb’** in the command prompt.
* You can execute the IRB (Interactive Ruby).
*	Enter **‘exit()’** in the IRB prompt.
* You can exit IRB.
![‘irb’ and 'exit()' in the command prompt](https://user-images.githubusercontent.com/32950391/80773508-1d045f80-8b28-11ea-872a-8c0255657a00.JPG)

12. Install Jekyll.
* Run **‘Command Prompt’**.
*	Enter **‘gem -v’** in the command prompt.
  - You can check the **installed version of ‘gem’**. – RubyGems is a package manager for the Ruby programming language.
![‘gem -v’ in the command prompt](https://user-images.githubusercontent.com/32950391/80774416-f562c680-8b2a-11ea-9da2-a93ced9f2d25.JPG)
* Enter **‘gem install jekyll bundler’** in the command prompt.
![‘gem install jekyll bundler’ in the command prompt](https://user-images.githubusercontent.com/32950391/80774527-48d51480-8b2b-11ea-951f-72a715941302.JPG)
*	Enter **‘jekyll -v’** in the command prompt.
  - You can check the installed **version of ‘jekyll’**.
![‘jekyll -v’ in the command prompt](https://user-images.githubusercontent.com/32950391/80774615-8174ee00-8b2b-11ea-9105-68951ae5b40f.JPG)
