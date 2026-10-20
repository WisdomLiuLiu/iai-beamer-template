IAI Beamer 基础模板

Overleaf 使用
1. 上传 IAI-Beamer-Template.zip，创建新项目。
2. 在项目设置中选择主文件 main.tex、编译器 XeLaTeX。
3. 点击一次 Recompile。目录及总页数所需的重复编译由 latexmk 自动完成。
   这里的“一次”指点击一次按钮，并非强制只运行一遍 TeX。

日常编辑只需修改 main.tex：
- 修改标题、作者、会议名称和日期。
- 长标题按可用宽度自动换行，不需要手动插入 \\；正文页眉为页码预留空间。
- 用 \section{Section title} 添加章节，目录及正文页眉第一行自动更新。
- 需要章节过渡页时，在 \section 后加 \IAISectionPage；否则可省略。
- 复制 \begin{frame}{Slide title} ... \end{frame} 添加正文页。
- 正文和各级列表已统一为默认字号，无需逐页添加 \large。
- 正文字体为 newtxtext/newtxmath，使用 11pt 文档字号与紧凑行距。
- 目录条目直接继承正文的字体与字号，正文样式调整后会同步更新。
- 如需额外的表格或绘图功能，可在 main.tex 导言区添加相应宏包。

文件
main.tex              报告信息与内容
beamerthemeIAI.sty     字体、间距、封面、目录、章节页、页眉及页码
latexmkrc             自动编译配置
assets/               两张官方 logo

本地编译：在项目目录运行 latexmk main.tex。
main.pdf 为编译预览，不需要上传到 Overleaf。

Logo 来源：合肥综合性国家科学中心人工智能研究院官网。
https://iai.ustc.edu.cn/r/cms/rgzn/default/Artificial-intelligence/img/AI-logo.png
https://iai.ustc.edu.cn/r/cms/rgzn/default/Artificial-intelligence/img/AI-footer-logo.png
