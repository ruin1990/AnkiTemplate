# ClozeAdv
Now, we can touch one by one cloze if a card have multi-clozes.
Original Github is [here](https://github.com/ruin1990/AnkiTemplate)

现在，如果一张卡片有多个完形填空，我们可以逐个触摸完形填空。
原始Github仓库在[这里](https://github.com/ruin1990/AnkiTemplate)

## Usage
> Choose one of the following methods
> 以下方法任选其一

1. You can import file AnkiTemplate_ClozeAdv.apkg or from [AnkiWeb](https://ankiweb.net/shared/info/457099967).

    您可以导入文件 AnkiTemplate_ClozeAdv.apkg 或从 [AnkiWeb](https://ankiweb.net/shared/info/457099967)。

2. Just change you own Cloze Template front content with my [front.html](https://github.com/ruin1990/AnkiTemplate/ClozeAdv/front.html).

    只需使用我的[front.html](https://github.com/ruin1990/AnkiTemplate/ClozeAdv/front.html)更改您自己的完形填空模板正面内容即可。


## Features
1. We can use touch/click/keyboard(Tab and Backquote) to reveal or cover the cloze.(Thanks: [kleinerpirat](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584))

    我们可以使用触摸/点击/键盘（Tab和反引号）来显示或覆盖完型填空。（感谢：[kleinerpirat](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584)）

2. If all the clozes are revealed, the card will auto flip to back.(Thanks: [git9527](https://github.com/git9527/anki-awesome-select))

    如果所有完形填空都被揭开，卡片会自动翻转到背面。（感谢： [git9527](https://github.com/git9527/anki-awesome-select)）

3. I add a float button view for reveal next cloze or cover previous cloze.(Thanks: [kleinerpirat](https://ankiweb.net/shared/info/1231171279))(Support English and Chinese automatically)

    我添加了一个浮动按钮视图，用于显示下一个完形填空或覆盖上一个完形填空。（感谢：[kleinerpirat](https://ankiweb.net/shared/info/1231171279))（自动支持英文和中文）

4. It can support multi-cloze separate by c[n], some template will convert all the c[n] to c1

    可以支持以c[n]分隔的多完形填空，有些模板会将所有c[n]转换为c1

5. Mathjax block is supported NOW!!!

    现在支持Mathjax 块！！！

> Demo for Mathjax
> Mathjax公式块示例

![mathjax](https://s2.loli.net/2022/01/18/bMEhgUJaDLcqk8r.gif)

> Demo for reciting Chinese
> 中文间隔记忆背诵示例

![demo](https://s3.bmp.ovh/imgs/2021/12/a08a795d540e1a09.gif)

## MathJax Bugs
MathJax is support NOW!!!

现在支持 MathJax 了！！！

but ClozeAdv cannot support multi-line MathJax formulation cloze or some complex span/div.

但 ClozeAdv 无法支持多行 MathJax 公式完形填空或某些复杂的 span/div。

See details with  [Current options to avoid](https://github.com/ruin1990/AnkiTemplate/issues/7).

详情请见：  [目前规避策略](https://github.com/ruin1990/AnkiTemplate/issues/7)

**For example:**

**举个例子：**

```
\[
\begin{aligned}
&{{c1::{\color{#C72929}{\|f+g\|_p = \left( \int_E |f+g|^p \, dx \right)^{1/p} }}}} \\
&= \left( \int_E |f|^p \, dx + \int_E |g|^p \, dx \right)^{1/p} \\
&\leq \|f\|_p + \|g\|_p
\end{aligned}
\]
```
### **1. Braces('{', '}') / 大括号**

Add a space between braces('{', '}') in the formula that are not used by cloze.
在公式中的大括号 ('{', '}') 之间添加完形填空未使用的空格。

![mathjax_issues](https://github.com/user-attachments/assets/e0829254-76dc-4f2d-87cf-b382bfdafba1)

### **2. Multi-line into Single-line / 多行重写为单行**

Rewrite multi-line Latex/Mathjax into one line, that is, remove the newline characters and put '\[' and '\]' on the same line

将多行Latex/Mathjax重写为一行，即去掉换行符，将'\['和'\]'放在同一行

Anki new version uses '<anki-mathjax>' and '</anki-mathjax>' instead of '\[' and '\]'

Anki 新版本使用 '<anki-mathjax>' 和 '</anki-mathjax>' 代替 '\[' 和 '\]'

```
<anki-mathjax>\begin{aligned} &amp;{{c1::{\color{#C72929}{\|f+g\|_p = \left( \int_E |f+g|^p \, dx \right)^{1/p} } } }} \\ &amp;= \left( \int_E |f|^p \, dx + \int_E |g|^p \, dx \right)^{1/p} \\ &amp;\leq \|f\|_p + \|g\|_p \end{aligned}</anki-mathjax> 
```

But when rendering, it is still in the Anki old format

但是渲染的时候还是使用Anki老格式

```
\[ \begin{aligned} &amp;{{c1::{\color{#C72929}{\|f+g\|_p = \left( \int_E |f+g|^p \, dx \right)^{1/p} } } }} \\ &amp;= \left( \int_E |f|^p \, dx + \int_E |g|^p \, dx \right)^{1/p} \\ &amp;\leq \|f\|_p + \|g\|_p \end{aligned} \]
```

### **3. Anki web version need refresh once / Anki网页版刷新一次**

If you use Anki web version, and the first card of each review has mathjax, the page should be refreshed once to take effect.(PR welcome)

如果您使用Anki网页版，并且每次学习的第一张卡片有mathjax，则需要刷新页面一次才能生效。 (欢迎大佬PR)

## Compatibility
| Platform | Support |
| ---- | ---- |
| Anki Droid     | **YES** |
|   Anki Mobile   | Issues with floating buttons, feedback & PR welcome |
|  Anki Windows    | **YES** |
|   Anki MacOS   |  Not test, feedback & PR welcome   |
|   Anki Linux   |  Not test, feedback & PR welcome   |
|   Web version   |  **YES**, with [mathjax bugs](#mathjax-bugs)  |

I would appreciate it if someone could give feedback on the results of compatibility

提前感谢未来的某位热心朋友就兼容性结果提供反馈

## License
Apache License V2.0

## Plus
If you find issues, please let me know. It's best to bring Anki Deck demo that can reproduce the problem

如果您发现错误，请告诉我。最好带上能重现该问题的Anki Deck demo

## Thanks & Reference
1. Keyboard support, 键盘支持[kleinerpirat](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584)
2. Auto flip to back, 自动翻面[git9527](https://github.com/git9527/anki-awesome-select)
3. Float button view, 悬浮按钮[kleinerpirat](https://ankiweb.net/shared/info/1231171279)
