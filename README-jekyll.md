# weibifan.github.io

Starter

### 基本概念：

- 有2种模式
- 一个仓库里面可以建立2目录（称为publishing source），docs或根目录，每个目录对应一个网站，需要在构建GitHub pages时指定。
  Configuring a publishing source for your GitHub Pages site
- 发布源的初始化需要在本地进行，然后上传到github目录下，再经过Jekyll生成静态文件，发布到GitHub.io上。
- jekyll默认构建一个博客网站。
- Host your site with services such as AWS Amplify, CloudCannon, Cloudflare Pages, GitHub Pages, GitLab Pages, and Netlify.
- Hugo说是简单，操作仍然很复杂 https://blog.csdn.net/leida_wt/article/details/104175919
- Hexo的主题一般只适合于写博客
- Theme和Template混用

模板：
https://github.com/topics/jekyll-theme

学术介绍模板：
https://github.com/RayeRen/acad-homepage.github.io
https://github.com/academicpages/academicpages.github.io

简单的模板：
https://github.com/ankitsultana/researcher
https://github.com/sharu725/online-cv

https://github.com/mmistakes/minimal-mistakes

博客模板：
https://github.com/mzlogin/mzlogin.github.io
https://github.com/xjtushilei/xjtushilei.github.io

https://themes.gohugo.io/themes/starter-hugo-academic/

### 2022-11-26

https://pages.github.com/
构建仓库，克隆到本地，生成index.html，更新到GitHub

https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll
一个列表，先读第1个链接，介绍GitHub Pages and Jekyll

阅读第2个链接，发现要安装Ruby和Jekyll
安装Ruby，发现下载很慢，Ruby的安装包在GitHub上，当然慢。
choco install ruby
中断安装，在Ruby网站找到exe安装包，下载，然后安装。
发现安装结束时，还要安装MSYS2，郁闷....

1 - MSYS2 base installation
2 - MSYS2 system update (optional)
3 - MSYS2 and MINGW development toolchain

Which components shall be installed? If unsure press ENTER [1,3] 1

MSYS2 seems to be unavailable
Download http://repo.msys2.org/distrib/x86_64/msys2-x86_64-20190524.exe
to C:\Users\Wei\AppData\Local\Temp/msys2-x86_64-20190524.exe
Installation failed: 404 Not Found

手工下载，放到指定的temp下，再次安装。
自动开始MSYS2的安装，66%时卡住好长时间，终于安装好了。

打开cmd with ruby
bundle version
gem -v

https://jekyllrb.com/docs/installation/
https://jekyllrb.com/docs/installation/windows/
发现上面安装是简版，不行，需要重新再来，卸载上面的ruby和msys2
重新安装Ruby + Devkit
rubyinstaller-devkit-3.1.2-1-x64

1 - MSYS2 base installation
2 - MSYS2 system update (optional)
3 - MSYS2 and MINGW development toolchain

Which components shall be installed? If unsure press ENTER [1,3] 3

> sh -lc true
> 'C:\WINDOWS\system32\drivers\etc\hosts' -> '/etc/hosts'
> 'C:\WINDOWS\system32\drivers\etc\protocol' -> '/etc/protocols'
> 'C:\WINDOWS\system32\drivers\etc\services' -> '/etc/services'
> 'C:\WINDOWS\system32\drivers\etc\networks' -> '/etc/networks'
> gpg: /etc/pacman.d/gnupg/trustdb.gpg：建立了信任度数据库
> gpg: 未找到任何绝对信任的密钥
> gpg: starting migration from earlier GnuPG versions
> gpg: porting secret keys from '/etc/pacman.d/gnupg/secring.gpg' to gpg-agent
> gpg: migration succeeded
> ==> 正在生成 pacman 主密钥。这可能需要一段时间。
> gpg: Generating pacman keyring master key...
> gpg: 密钥 76E9CF1739176C3F 被标记为绝对信任
> gpg: 目录‘/etc/pacman.d/gnupg/openpgp-revocs.d’已创建
> gpg: 吊销证书已被存储为‘/etc/pacman.d/gnupg/openpgp-revocs.d/225BEC58FE772338D4571B2276E9CF1739176C3F.rev’
> gpg: Done
> ==> 正在更新可信数据库...
> gpg: marginals needed: 3  completes needed: 1  trust model: pgp
> gpg: 深度：0  有效性：  1  已签名：  0  信任度：0-，0q，0n，0m，0f，1u
> ==> 正在从 msys2.gpg 添加密匙...

MSYS2 and MINGW development tool chain

打开cmd with ruby
提示：ruby 3.1.2p20 (2022-04-12 revision 4491bb740a) [x64-mingw-ucrt]

gem install jekyll bundler    好长时间没有响应，过了大概10分钟才有提示。
C:\Users\Wei>gem install jekyll bundler
Fetching webrick-1.7.0.gem
Fetching terminal-table-3.0.2.gem
Fetching unicode-display_width-2.3.0.gem
...
webrick, unicode-display_width, terminal-table, safe_yaml, rouge, forwardable-extended, pathutil, mercenary, liquid, kramdown, kramdown-parser-gfm, ffi, rb-inotify, rb-fsevent, listen, jekyll-watch, sassc, jekyll-sass-converter, concurrent-ruby, i18n, http_parser.rb, eventmachine, em-websocket, colorator, public_suffix, addressable, jekyll

最后是安装了29个包。

jekyll -v
jekyll 4.3.1

cd C:\Users\Wei\PycharmProjects\weibifan.github.io
mkdir docs

C:\Users\Wei\PycharmProjects\weibifan.github.io\docs>jekyll new --skip-bundle .
注意一定要加.  否则出错：
jekyll 4.3.1 | Error:  You must specify a path.
C:/Ruby31-x64/lib/ruby/gems/3.1.0/gems/jekyll-4.3.1/lib/jekyll/commands/new.rb:25:in `process': You must specify a path. (ArgumentError)

按说明修改Gemfile
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll

bundle install
后面没有.   加挂代理，又安装了几十个包。。。

本地测试：
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll

bundle add webrick

bundle exec jekyll serve

浏览器打开： http://127.0.0.1:4000/

commit 内容

在Github上设置为docs
