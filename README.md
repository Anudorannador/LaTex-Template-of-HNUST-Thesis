湖南科技大学毕业设计LaTex模板
===

## 说明：
这个模板是根据[湖南科技大学毕业设计（论文）格式要求](http://jwc.hnust.cn/Uploadfiles/files/20141201172656805.doc)设计出来的LaTeX模板，这样老师就再也不用为我们的格式操心了。
如果有任何疑问，请邮件咨询：<freagle@yeah.net>，注意邮件主题：湖南科技大学毕业设计（论文）LaTeX模板

## 使用方法

### 准备工作：
1. 进入[fonts](./fonts)目录，将下面三个字体安装好。
2. 进入[docs](./docs)目录，将frontpages.docx里面的扉页、任务书等内容填写好，并在该目录下生成frontpages.pdf。
3. 进入[tex](./tex)目录，main.tex 是主tex文档。

### 编译文档：
 - 编译要求使用 `xelatex` 和 `bibtex` 两个命令。
 - [tex](./tex) 下有个[Makefile](./tex/Makefile)文件，Linux和Mac OS的用户可以直接运行`make`命令进行编译，生成一个对应的pdf文档，当然`make clean`会删除编译信息，请注意，包括 pdf 文档。不知Makefile为何物的同学可忽略此信息，感谢您的阅读。
 - 手动编译：因为LaTeX的性质，所以先编译一次文档，再编译一次文献，再编译两次文档，所以就是：`xelatex main && bibtex main && xelatex main && xelatex main`。
 - 如果编译的时候不需要扉页、任务书这些信息，可以把[./tex/main.tex](./tex/main.tex)文件114行的`\includepdf[pages={1-}]{../docs/frontpages.pdf}`那行命令注释掉；或者自己修改需要打印哪些页。

## 感谢
感谢 [GB/T7714-2005 bst文件](https://github.com/Haixing-Hu/GBT7714-2005-BibTeX-Style)的提供者[Haixing-Hu](https://github.com/Haixing-Hu)。

感谢长者。

