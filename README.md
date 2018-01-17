# EvanLi.github.io
My first github pages
# 一、标题
在 Markdown 中，你只需要在文本前面加上 # 即可，同理、你还可以增加二级标题、三级标题、四级标题、五级标题和六级标题，总共六级，只需要增加 # 即可，标题字号相应降低。例如：
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
 *注：#和「一级标题」之间建议保留一个字符的空格，这是最标准的 Markdown 写法。*
# 二、列表   
*列表格式也很常用，在 Markdown 中，你只需要在文字前面加上 - 就可以了，例如:*
- 文本1
- 文本2
- 文本3

*如果你希望有序列表，也可以在文字前面加上 1. 2. 3. 就可以了，例如:*
1. 文本1
2. 文本2
3. 文本3

# 三、链接
*在 Markdown 中，插入链接不需要其他按钮，你只需要使用 [显示文本](链接地址) 这样的语法即可，例如:*
[简书](http://www.jianshu.com)
# 四、图片
在 Markdown 中，插入图片不需要其他按钮，你只需要使用

` ![](图片链接地址) 这样的语法即可，例如： `
` ![图片测试](http://ww4.sinaimg.cn/bmiddle/aa397b7fjw1dzplsgpdw5j.jpg "Optional title") `

**效果如下**

![图片测试](http://ww4.sinaimg.cn/bmiddle/aa397b7fjw1dzplsgpdw5j.jpg "Optional title")

* 图片加链接如下格式：*

`[![图片测试](http://ww4.sinaimg.cn/bmiddle/aa397b7fjw1dzplsgpdw5j.jpg)](http://www.jianshu.com)`
[![图片测试](http://ww4.sinaimg.cn/bmiddle/aa397b7fjw1dzplsgpdw5j.jpg)](http://www.jianshu.com)
# 五、引用
*在我们写作的时候经常需要引用他人的文字，这个时候引用这个格式就很有必要了，在 Markdown 中，你只需要在你希望引用的文字前面加上 > 就好了，例如：*
*注：>和文本之间要保留一个字符的空格。*
如：
` > 一盏灯， 一片昏黄； 一简书， 一杯淡茶。 守着那一份淡定， 品读属于自己的寂寞。 保持淡定， 才能欣赏到最美丽的风景！ 保持淡定， 人生从此不再寂寞。`
显示的是：
> 一盏灯， 一片昏黄； 一简书， 一杯淡茶。 守着那一份淡定， 品读属于自己的寂寞。 保持淡定， 才能欣赏到最美丽的风景！ 保持淡定， 人生从此不再寂寞。  

# 六、粗体和斜体
*Markdown 的粗体和斜体也非常简单，用两个 \* 包含一段文本就是粗体的语法，用一个 \* 包含一段文本就是斜体的语法。例如：*
`*一盏灯， 一片昏黄；， 一杯淡茶。 守着那一份淡定， 品读属于自己的寂寞。 保持淡定， 才能欣赏到最美丽的风景！ 保持淡定， 人生从此不再寂寞。*`
`**简书**`
**显示效果**
*一盏灯， 一片昏黄；， 一杯淡茶。 守着那一份淡定， 品读属于自己的寂寞。 保持淡定， 才能欣赏到最美丽的风景！ 保持淡定， 人生从此不再寂寞。*
**简书**
# 七、代码引用
需要引用代码时，如果引用的语句只有一段，不分行，可以用 ` 将语句包起来。如果引用的语句为多行，可以将```置于这段代码的首行和末行。

**示例1:**           

` \`Hello World\` `
显示：     `Hello World`

**示例2：**
```
代码1
代码2
代码3
```
# 八、表格
*相关代码：（注意表格上要空一行，代码不需要对齐，表格对齐方式由：决定）*
```
| Tables            | Are              | Cool      |
| -------------- | :--------------: | --------: |
| col 3 is          | right-aligned    | $1600     |
| col 2 is          | centered         | $12       |
| zebra stripes     | are neat         | $1        |
```
 *显示效果 *

| Tables            | Are              | Cool      |
| :----------- | :----------: | ------: |
| col 3 is        | right-aligned    | $1600     |
| col 2 is          | centered         | $12       |
| zebra stripes     | are neat         | $1        |
*相关代码：*
```
dog | bird | cat
----|------|----
foo | foo | foo
bar | bar | bar
baz | baz | baz
```
显示效果

dog | bird | cat
----|------|----
foo | foo | foo
bar | bar | bar
baz | baz | baz

右对齐：

a|b |c |
---:|---:|---:
a|b|c
左对齐：

a|b |c |
:---|:---|:---
a|b|c
居中：

a|b |c |
:---:|:---:|:---:
a|b|c
