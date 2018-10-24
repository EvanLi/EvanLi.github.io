---
layout: post
title: Jupyter NoteBook的快捷键使用指南
date: 2018-10-24
categories: blog
tags: [jupyter]
description: Jupyter NoteBook 的快捷键使用指南
---


# Jupyter NoteBook 的快捷键使用指南

转载自：[Jupyter NoteBook 的快捷键使用指南](http://opus.konghy.cn/ipynb/jupyter-notebook-keyboard-shortcut.html)

---
Jupyter Notebook 有两种键盘输入模式。即命令模式和编辑模式，这与 [Vim](http://www.vim.org/) 有些类似。在编辑模式下，可以往单元中键入代码或文本，此时单元格被绿色的框线包围，且命令模式下的快捷键不生效。在命令模式下，可以用快捷键命令运行单元格，移动单元格，切换单元格编辑状态等等，此时的单元格被灰色的框线包围，且编辑模式下的快捷键不生效。

从命令模式进入编辑模式需按 `Enter` 键，从编辑模式切换到命令模式需按 `Esc` 键。

以下两表分别是对命令和编辑两种模式下快捷键的简单说明：

## 命令模式快捷键（按 Esc 键开启）:

|快捷键|作用|说明|
|---|---|---|
|Enter|转入编辑模式||
|Shift-Enter|运行本单元，选中下个单元|新单元默认为命令模式|
|Ctrl-Enter|运行本单元||
|Alt-Enter|运行本单元，在其下插入新单元|新单元默认为编辑模式|
|Y|单元转入代码状态||
|M|单元转入 markdown 状态||
|R|单元转入 raw 状态||
|1|设定1级标题|仅在markdown状态下时建议使用标题相关快捷键，|
|2|设定2级标题|如果单元处于其他状态，|
|3|设定3级标题|则会强制切换到markdown状态|
|4|设定4级标题||
|5|设定5级标题||
|6|设定6级标题||
|Up|选中上方单元||
|K|选中上方单元||
|Down|选中下方单元||
|J|选中下方单元||
|Shift-K|连续选择上方单元||
|Shift-J|连续选择下方单元||
|A|在上方插入新单元||
|B|在下方插入新单元||
|X|剪切选中的单元||
|C|复制选中的单元||
|Shift-V|粘贴到上方单元||
|V|粘贴到下方单元||
|Z|恢复删除的最后一个单元||
|D,D|删除选中的单元|连续按两个 D 键|
|Shift-M|合并选中的单元||
|Ctrl-S|保存当前 NoteBook||
|S|保存当前 NoteBook||
|L|开关行号|编辑框的行号是可以开启和关闭的|
|O|转换输出||
|Shift-O|转换输出滚动||
|Esc|关闭页面||
|Q|关闭页面||
|H|显示快捷键帮助||
|I,I|中断 NoteBook 内核||
|0,0|重启 NoteBook 内核||
|Shift|忽略||
|Shift-Space|向上滚动||
|Space|向下滚动||

## 编辑模式快捷键（ 按 Enter 键启动）:

|快捷键|作用|说明|
|---|---|---|
|Tab|代码补全或缩进||
|Shift-Tab|提示|输出帮助信息，部分函数、类、方法等会显示其定义原型，如果在其后加 `?` 再运行会显示更加详细的帮助|
|Ctrl-]|缩进|向右缩进|
|Ctrl-[|解除缩进|向左缩进|
|Ctrl-A|全选||
|Ctrl-Z|撤销||
|Ctrl-Shift-Z|重做||
|Ctrl-Y|重做||
|Ctrl-Home|跳到单元开头||
|Ctrl-Up|跳到单元开头||
|Ctrl-End|跳到单元末尾||
|Ctrl-Down|跳到单元末尾||
|Ctrl-Left|跳到左边一个字首||
|Ctrl-Right|跳到右边一个字首||
|Ctrl-Backspace|删除前面一个字||
|Ctrl-Delete|删除后面一个字||
|Esc|切换到命令模式||
|Ctrl-M|切换到命令模式||
|Shift-Enter|运行本单元，选中下一单元|新单元默认为命令模式|
|Ctrl-Enter|运行本单元||
|Alt-Enter|运行本单元，在下面插入一单元|新单元默认为编辑模式|
|Ctrl-Shift--|分割单元|按光标所在行进行分割|
|Ctrl-Shift-Subtract|分割单元||
|Ctrl-S|保存当前 NoteBook||
|Shift|忽略||
|Up|光标上移或转入上一单元||
|Down|光标下移或转入下一单元||
|Ctrl-/|注释整行/撤销注释|仅代码状态有效|

**注：** 如果快捷键被系统中的其它应用占用，则可能会失效