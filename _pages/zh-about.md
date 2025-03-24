---
permalink: /zh/
title: "AIEvoMed"
author_profile: true
redirect_from:
  - /zh/about/
  - /zh/about.html
---

这是网站的首页，它由 [Academic Pages 模板](https://github.com/academicpages/academicpages.github.io) 驱动并托管在 GitHub Pages 上。[GitHub Pages](https://pages.github.com) 是一项免费服务，网站从存储在 GitHub 仓库中的代码和数据构建和托管，并在每次向仓库提交新内容时自动更新。此模板 Fork 自 Michael Rose 创建的 [Minimal Mistakes Jekyll 主题](https://mmistakes.github.io/minimal-mistakes/)，并进行了扩展，以支持学者拥有的各种内容：出版物、演讲、教学、作品集、博客文章和动态生成的 CV。您可以立即 Fork [此模板](https://github.com/academicpages/academicpages.github.io)，修改配置和 Markdown 文件，添加您自己的 PDF 和其他内容，并免费拥有自己的网站，没有广告！

数据驱动的个人网站
======
像许多其他基于 Jekyll 的 GitHub Pages 模板一样，Academic Pages 使您将网站的内容与其形式分离。您网站的内容和元数据位于结构化的 Markdown 文件中，而各种其他文件构成了主题，指定了如何将该内容和元数据转换为 HTML 页面。您将这些各种 Markdown (.md)、YAML (.yml)、HTML 和 CSS 文件保存在公共 GitHub 存储库中。每次您提交并推送对存储库的更新时，[GitHub Pages](https://pages.github.com/) 服务都会基于这些文件创建静态 HTML 页面，这些页面免费托管在 GitHub 的服务器上。

动态内容管理系统（如 Wordpress）的许多功能都可以通过这种方式实现，使用的计算资源更少，并且更不容易受到黑客攻击和 DDoS 攻击。您还可以随意修改主题，而无需触及网站的内容。如果您到了无法修复 Jekyll/HTML/CSS 中某些问题的地步，那么描述您的演讲、出版物等的 Markdown 文件是安全的。您可以回滚更改，甚至删除存储库并重新开始 - 只需确保保存 Markdown 文件即可！最后，您还可以编写脚本来处理站点上的结构化数据，例如[这个脚本](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb)，它分析关于演讲页面的元数据以显示[您发表演讲的每个地点的地图](https://academicpages.github.io/talkmap.html)。

开始使用
======
1. 如果您没有 GitHub 帐户，请注册一个并确认您的电子邮件（必需！）
2. 通过单击右上角的“使用此模板”按钮 Fork [此模板](https://github.com/academicpages/academicpages.github.io)。
3. 转到存储库的设置（以“代码”开头的选项卡中最右边的项目，应在“取消监视”下方）。将存储库重命名为“[您的 GitHub 用户名].github.io”，这也将是您网站的 URL。
4. 设置站点范围的配置并创建内容和元数据（见下文 - 另请参阅[这组差异](http://archive.is/3TPas)，显示了为用户名为“getorg-testacct”的用户设置[示例站点](https://getorg-testacct.github.io)而更改的文件）
5. 将任何文件（如 PDF、.zip 文件等）上传到 files/ 目录。它们将显示在 https://[您的 GitHub 用户名].github.io/files/example.pdf。
6. 通过转到存储库设置中的“GitHub Pages”部分来检查状态

站点范围配置
------
该站点的主要配置文件位于基本目录中的 [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml) 中，它定义了侧边栏和其他站点范围功能中的内容。您需要将默认变量替换为您自己和您网站的 github 存储库的变量。顶部菜单的配置文件位于 [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml) 中。例如，如果您没有作品集或博客文章，您可以从 navigation.yml 文件中删除这些项目，以将其从标题中删除。

创建内容和元数据
------
对于站点内容，每种内容类型都有一个 Markdown 文件，这些文件存储在 _publications、_talks、_posts、_teaching 或 _pages 等目录中。例如，每次演讲都是 [_talks 目录](https://github.com/academicpages/academicpages.github.io/tree/master/_talks) 中的 Markdown 文件。在每个 Markdown 文件的顶部，都有关于演讲的 YAML 结构化数据，主题将解析这些数据以执行许多很酷的操作。关于演讲的相同结构化数据用于生成 [演讲页面](https://academicpages.github.io/talks) 上的演讲列表、特定演讲的每个[单独页面](https://academicpages.github.io/talks/2012-03-01-talk-1)、[CV 页面](https://academicpages.github.io/cv) 的演讲部分以及[您发表演讲的地点的地图](https://academicpages.github.io/talkmap.html)（如果您运行[此 python 文件](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) 或 [Jupyter 笔记本](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb)，它会根据 _talks 目录的内容创建地图的 HTML）。

**Markdown 生成器**

该存储库包含 [一组 Jupyter 笔记本](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator)，可将包含关于演讲或演示文稿的结构化数据的 CSV 转换为单独的 Markdown 文件，这些文件将针对 Academic Pages 模板进行正确格式化。该目录中的示例 CSV 是我用来创建我在 stuartgeiger.com 上的个人网站的 CSV。我通常的工作流程是，我保留我的出版物和演讲的电子表格，然后运行这些笔记本中的代码来生成 Markdown 文件，然后提交并将它们推送到 GitHub 存储库。

如何编辑您网站的 GitHub 存储库
------
许多人使用 git 客户端在本地计算机上创建文件，然后将它们推送到 GitHub 的服务器。如果您不熟悉 git，您可以直接在 github.com 界面中编辑这些配置文件和 Markdown 文件。导航到文件（如[此文件](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md)），然后单击内容预览右上角的铅笔图标（在“Raw | Blame | History”按钮的右侧）。您可以通过单击铅笔图标右侧的垃圾桶图标来删除文件。您还可以通过导航到目录并单击“创建新文件”或“上传文件”按钮来创建新文件或上传文件。

示例：编辑演讲的 Markdown 文件
![编辑演讲的 Markdown 文件](/images/editing-talk.png)

更多信息
------
有关配置 Academic Pages 的更多信息，请参见[指南](https://academicpages.github.io/markdown/)、[不断增长的 Wiki](https://github.com/academicpages/academicpages.github.io/wiki)，您始终可以在 [GitHub 上提问](https://github.com/academicpages/academicpages.github.io/discussions)。[Minimal Mistakes 主题](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)（此主题由此 Fork 而来）的指南也可能有所帮助。

