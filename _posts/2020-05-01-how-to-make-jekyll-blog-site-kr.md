---
title: "윈도우10에서 Jekyll 블로그 사이트를 만드는 방법"
categories: [Jekyll]
tags: [Ruby, Jekyll, blog, Jekyll blog, Jekyll site]
---

## 윈도우10에서 Jekyll 블로그 사이트를 만드는 방법

1. **‘명령 프롬프트’**를 실행하십시오.
* 명령 프롬프트에서 **‘jekyll -v’**를 입력하십시오.
  - 설치된 ‘jekyll’의 **버전**을 확인할 수 있습니다.
* 만약 Jekyll의 버전을 확인할 수 없다면, [윈도우10에 Ruby와 Jekyll을 설치하는 방법](/jekyll/how-to-install-ruby-and-jekyll-on-windows-10-kr/) 페이지로 가서 먼저 **'Ruby'와 'Kekyll'** 를 설치하십시오.
```
C:\>jekyll -v
jekyll 4.0.0    
C:\>
```

2. Jekyll 블로그 사이트를 만들길 원하는 **디렉터리**로 이동하십시오.
* 디렉터리가 존재하지 않는다면, 디렉터리를 만들 수 있습니다.
```
C:\>mkdir jekyll_dir
C:\>cd jekyll_dir
C:\jekyll_dir>
```

3. 명령 프롬프트에서 **‘jekyll new my-blog-site’**를 입력하십시오.
* 'my-blog-site'는 **디렉터리**이며, 필요시 생성될 것입니다.
```
C:\jekyll_dir>jekyll new my-blog-site
Running bundle install in C:/jekyll/my-blog-site...
  Bundler: Fetching gem metadata from https://rubygems.org/...........
  Bundler: Fetching gem metadata from https://rubygems.org/.
  Bundler: Resolving dependencies...
  Bundler: Using public_suffix 4.0.4
  Bundler: Using addressable 2.7.0
  Bundler: Using bundler 2.1.4
  Bundler: Using colorator 1.1.0
  Bundler: Using concurrent-ruby 1.1.6
  Bundler: Using eventmachine 1.2.7 (x64-mingw32)
  Bundler: Using http_parser.rb 0.6.0
  Bundler: Using em-websocket 0.5.1
  Bundler: Using ffi 1.12.2 (x64-mingw32)
  Bundler: Using forwardable-extended 2.6.0
  Bundler: Using i18n 1.8.2
  Bundler: Using sassc 2.3.0 (x64-mingw32)
  Bundler: Using jekyll-sass-converter 2.1.0
  Bundler: Fetching rb-fsevent 0.10.4
  Bundler: Installing rb-fsevent 0.10.4
  Bundler: Using rb-inotify 0.10.1
  Bundler: Using listen 3.2.1
  Bundler: Using jekyll-watch 2.2.1
  Bundler: Using rexml 3.2.4
  Bundler: Using kramdown 2.2.1
  Bundler: Using kramdown-parser-gfm 1.1.0
  Bundler: Using liquid 4.0.3
  Bundler: Using mercenary 0.3.6
  Bundler: Using pathutil 0.16.2
  Bundler: Using rouge 3.18.0
  Bundler: Using safe_yaml 1.0.5
  Bundler: Using unicode-display_width 1.7.0
  Bundler: Using terminal-table 1.8.0
  Bundler: Using jekyll 4.0.0
  Bundler: Using jekyll-feed 0.13.0
  Bundler: Using jekyll-seo-tag 2.6.1
  Bundler: Using minima 2.5.1
  Bundler: Using thread_safe 0.3.6
  Bundler: Using tzinfo 1.2.7
  Bundler: Using tzinfo-data 1.2020.1
  Bundler: Using wdm 0.1.1
  Bundler: Bundle complete! 6 Gemfile dependencies, 35 gems now installed.
  Bundler: Use `bundle info [gemname]` to see where a bundled gem is installed.
New jekyll site installed in C:/jekyll_dir/my-blog-site.
C:\jekyll_dir>
```

4. 생성된 **디렉터리**로 이동하고 사이트를 생성합니다.
* 명령 프롬프트에서 **‘cd my-blog-site’**를 입력하십시오.
* 명령 프롬프트에서 **‘bundle exec jekyll serve’**를 입력하십시오.
```
C:\jekyll_dir>cd my-blog-site
C:\jekyll_dir\my-blog-site>bundle exec jekyll serve
Configuration file: C:/jekyll_dir/my-blog-site/_config.yml
            Source: C:/jekyll_dir/my-blog-site
       Destination: C:/jekyll_dir/my-blog-site/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 2.681 seconds.
 Auto-regeneration: enabled for 'C:/jekyll_dir/my-blog-site'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

5. 웹브라우저에서 **<http://localhost:4000>**로 이동합니다.
* 블로그 사이트를 볼 수 있습니다.
![Jekyll blog site localhost 4000](https://user-images.githubusercontent.com/32950391/80854011-db94b280-8c02-11ea-848c-990973884176.JPG)
