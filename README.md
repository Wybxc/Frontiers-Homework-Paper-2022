# 前沿计算研究实践期末论文作业

## 配置

推荐使用 [VSCode](https://code.visualstudio.com/) 编辑器，安装 [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) 插件。

此项目中已包含 LaTeX Workshop 的推荐工作区配置文件。

## 编译

使用 XeLaTeX 与 BibTeX 编译，命令如下：

```sh
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -synctex=1 main.tex
bibtex main
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -synctex=1 main.tex
xelatex -interaction=nonstopmode -halt-on-error -file-line-error -synctex=1 main.tex
```

## 持续集成

已配置 [GitHub Actions](https://github.com/Wybxc/Frontiers-Homework-Paper-2022/actions/workflows/latex.yml) 自动编译。

可以在 Actions 页面的 artifacts 中下载编译后的 PDF 文件。

## 文件结构

使用 [subfiles](https://ctan.org/pkg/subfiles) 宏包，每一节的内容放在 `sections` 目录下的单独文件中，`main.tex` 为主文件，包含所有章节。

```sh
.
├── main.tex
├── reference.bib
├── sections
│   ├── abstract.tex
│   ├── intro.tex
│   ├── related.tex
│   ├── git-workflows.tex
│   ├── modern-OSS.tex
|   ├── tips.tex
│   └── conclusion.tex
└── README.md
```

## 参考文献

见 `reference.bib`。

## 许可

作者保留所有权利。未经允许，不得转载、引用、修改或用于商业用途。
