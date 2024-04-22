# HITsz 信号与系统实验报告 $\LaTeX$ 模板

## 简介

本仓库如题所述, 为该课程提供 $\LaTeX$ 空白模板, 供学生填写实验内容后提交给老师.

本仓库在[此仓库](https://github.com/LittleYe233/hitsz-physics-ib-reports)的基础上作修改. 有兴趣可以参观本系列实验报告的最初模板.

## 编译

仓库拥有者的编译环境为 Arch Linux + TeX Live. 请用户尽可能使用最新版的 TeX Live.

### 准备

编译前需要对字体做出准备. 字体来源于 Google Noto CJK ([Serif](https://github.com/notofonts/noto-cjk/releases/download/Serif2.002/09_NotoSerifCJKsc.zip) 与 [Sans](https://github.com/notofonts/noto-cjk/releases/download/Sans2.004/08_NotoSansCJKsc.zip)) 和方正楷体 (恕不提供下载链接). 下载相应字体后请将其放入该仓库下的 `fonts` 文件夹.

若需要代码显示支持 (部分实验可能需要在实验报告中附代码), 请在 `*.cls` 文件下找到

```latex
% \RequirePackage[newfloat]{minted}
```

和

```latex
% \setminted{linenos, breaklines, frame=lines}
% \SetupFloatingEnvironment{listing}{name={程序清单}}

% \setmonofont{LigalexMono}[
%     Path=fonts/,
%     Extension=.ttf,
%     ItalicFont=LigalexMono-Italic,
%     BoldFont=LigalexMono-Bold
% ]
```

部分, 将其取消注释即可. 这需要 [minted](http://mirrors.ctan.org/macros/latex/contrib/minted/minted.pdf) 包的支持. 该部分系仓库拥有者个人喜好而写成, 用户可以自行修改. 此处亦使用了 Ligalex Mono 字体用以显示代码, 用户若需要可以自行下载放入 `fonts` 文件夹中.

此时, `fonts` 文件夹下的文件列表如下所示:

- FZKTK.TTF
- LigalexMono-Italic.ttf
- NotoSansCJKsc-Bold.otf
- NotoSerifCJKsc-Bold.otf
- LigalexMono-Bold.ttf
- LigalexMono.ttf
- NotoSansCJKsc-Regular.otf
- NotoSerifCJKsc-Regular.otf

特别注明: 实验报告的默认字体为 Noto Serif CJK SC 大小 10.5pt.

### 编译命令

在该仓库根目录下, 执行

```bash
latexmk -shell-escape -synctex=1 -interaction=nonstopmode -file-line-error -xelatex {文件名}
```

即可. `{文件名}` 例如 `report-1.tex`.

## 与 Word 原始模板的区别

本仓库在仓库拥有者能力下尽可能贴近原始的 Word 模板, 但同时考虑到个人喜好之内, 这仍与原始模板有一些不同之处, 包括但不限于:

- 一些边框的宽度, 边距存在不同;
- 一些字体和字号存在不同;
- 问题下方没有足够的空白, 需要用户自行阅读实验报告源码, 找到需要填充内容的位置.

虽然存在不同, 但本仓库将尽最大可能保证用户的实验报告可以通过. 若不能通过, 烦请联系仓库拥有者或提交 PR.

## 进度

- ✔️ 实验一
- ✔️ 实验二
- ✔️ 实验三
- ❎️ 实验四
- ❎️ 实验五
- ❎️ 实验六
- ❎️ 实验七
- ❎️ 实验八
- ❎️ 实验九
- ❎️ 实验十

## 测试

❎️ 经过仓库拥有者或他人测试, 证明老师可以接受该模板

## 使用和引用

您作为使用者可以直接使用本仓库的任何内容. 引用仓库拥有者名下的实验报告系列仓库只需要在任何一个仓库下提交 issue 说明即可, 一旦同意引用即表明您可以引用该系列的任何仓库.
