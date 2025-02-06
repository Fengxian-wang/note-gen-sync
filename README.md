# Academic Pages

![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)

Academic Pages is a Github Pages template for academic websites.

# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Running Locally

When you are initially working your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.
1. Make sure you have ruby-dev, bundler, and nodejs installed
    
    On most Linux distribution and [Windows Subsystem Linux](https://learn.microsoft.com/en-us/windows/wsl/about) the command is:
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    On MacOS the commands are:
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

If you are running on Linux it may be necessary to install some additional dependencies prior to being able to run locally: `sudo apt install build-essential gcc make`

# Maintenance

Bug reports and feature requests to the template should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.





很多朋友到了本科生或者研究生或者博士生的高年级，有了制作个人主页的需求，今天这一期博客将以academicpages模板为例，手把手教你快速制作一个简洁能用的个人主页。



1.首先你需要拥有一个github账号

2.然后我们来找模板，比如你可以在[Jekyll Themes](http://jekyllthemes.org/)

找到很多美丽的模板，但是我们这里着重细致地教一个简单的，如果你对模板没什么特殊的偏好并且不太想大费周章，这篇文章将会很好地满足你的需求。

点击网址https://github.com/academicpages/academicpages.github.io

 这个就是我们即将使用的模板

![img](https://img-blog.csdnimg.cn/021df64c7b92411ebe719b4ed513924e.png)

3.点击fork

![img](https://img-blog.csdnimg.cn/3200307530024b82b723322c4574d9b9.png)

 在repository name里填入yourname.github.io

比如我的github name是QiuDi233，那么这里我就要填入QiuDi233.github.io

4.按顺序点击以下按钮，修改Branch为master /root 然后点击save 

![img](https://img-blog.csdnimg.cn/a1b63b864ce445f994ecc2810401205f.png)

等待一会儿之后就会看到这个

![img](https://img-blog.csdnimg.cn/ef36da137d4a4667bf3a56ad13885bac.png)



此时我们点击这个网址已经可以看到个人主页了，显示的是默认的模板

![img](https://img-blog.csdnimg.cn/3b02dc2de3e74fe48d022c0ab6a79555.png)

 5.接下来我们再根据自己的个人信息来修改这个模板

![img](https://img-blog.csdnimg.cn/e05d03cab809496d9b2952c7342a46d5.png)

 要修改这个地方，我们找到yourname.github.io/_pages/about.md

![img](https://img-blog.csdnimg.cn/4a08d09232244c33b4c9579f2533135d.png)

 ![img](https://img-blog.csdnimg.cn/2f720040462f4dc79b0c0f9ca18bffd7.png)

 ![img](https://img-blog.csdnimg.cn/1adbc82f009e4056b7bcde3c2c4af468.png)

 照着它的格式用[markdown语法](https://so.csdn.net/so/search?q=markdown语法&spm=1001.2101.3001.7020)书写自己的个人信息

比如我这里给出一个例子：

I'm a third year undergraduate student from [School of EECS](https://eecs.pku.edu.cn/), [Peking University](https://www.pku.edu.cn/). My research interest includes computer vision, computer graphics, machine learning, and computational photography.

I am very fortunate to be advised by [Prof. XXX](https://www.XXX.com/) of XXX [Lab](https://so.csdn.net/so/search?q=Lab&spm=1001.2101.3001.7020) from [School of Computer Science](https://cs.pku.edu.cn/), Peking University. I was advised by [Prof. XX](https://XXX.pku.edu.cn/) from [School of Computer Science](https://cs.pku.edu.cn/), Peking University.

You can find my CV here: [XX's Curriculum Vitae](../assets/Curriculum_Vitae.pdf).

[Email](mailto:XX@stu.pku.edu.cn) / [Github](https://github.com/QiuDi233) / [Wechat](../images/wechat.jpg) / [CSDN](https://blog.csdn.net/qd1813100174?spm=1000.2115.3001.5343)

![img](https://img-blog.csdnimg.cn/13dba3d6d10a47ee845d39cf71dcc3a5.png)



然后我们在image文件夹中上传提到过的照片，比如我这里提到了微信，我就上传我的微信二维码，并且其命名为wechat.jpg

![img](https://img-blog.csdnimg.cn/e8953780e5934c25811bcdf9aa70e3f4.png)

 再比如我提到了我的CV在../assets/Curriculum_Vitae.pdf，那么我们就将Curriculum_Vitae.pdf文件传到assets文件夹里

![img](https://img-blog.csdnimg.cn/b4fb5aae09bd425090885f89e072484a.png)

 然后我们再来改左侧栏

![img](https://img-blog.csdnimg.cn/d15af77d6d314c8e85ef64566d1c4531.png)

 找到文件_config.yml

![img](https://img-blog.csdnimg.cn/239c732bb3484112ac00294b551997ff.png)

 网址和照片文件按需改成自己的，照片文件改完名字之后记得上传到image文件夹里。

注意：_config.yml文件中的这个地方要修改，**不然你的照片会无法显示**（笔者在这里踩坑了快一个小时）

![img](https://img-blog.csdnimg.cn/30558734e464461e8b24c815613ebc7c.png)

 并且照片要png格式的，不要jpg格式的！

 ![img](https://img-blog.csdnimg.cn/454f58fe636b4d2c909f6e04ddb4dec7.png)

 解决方法：![img](https://img-blog.csdnimg.cn/deb4ae094c104314bad9fe4796807f72.png)

这个问题的链接： [images not showing in sidebar · Issue #91 · academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io/issues/91)



不需要的功能可以注释掉掉，比如我没有Google scholar就直接把网址前加上#注释掉。

![img](https://img-blog.csdnimg.cn/0e66595a3e484490afdbbb82c5a189f2.png)

 我修改完之后如下，供参考：

![img](https://img-blog.csdnimg.cn/14bf3295f6f5486ca34899857fe1812b.png)

 

 至此，主页的第一页已经修改好了，我们再来修改最上面一栏点击之后会跳转的内容。

![img](https://img-blog.csdnimg.cn/16c58b9cef154069a0d148fc02b5686c.png)

 直接修改对应的文件夹中的内容

![img](https://img-blog.csdnimg.cn/19f5b9113cec4cc4b3a5993244aae8a4.png)



![img](https://img-blog.csdnimg.cn/827fe7c0fe704ca29c76eaacf88074d5.png)

如果有不需要的栏目可以在这里进行删除

![img](https://img-blog.csdnimg.cn/2d91bfc1d9264d529b64899a052cd30d.png)





 至此，一个基础的个人主页就做好了。

![img](https://img-blog.csdnimg.cn/6645a5a25c25484289f0b4ee23b3d001.png)
