# ClozeAdv
Now, we can touch one by one cloze if a card have multi-clozes.
Original Github is [here](https://github.com/ruin1990/AnkiTemplate)

## Usage
1. You can import file AnkiTemplate_ClozeAdv.apkg or from [AnkiWeb](https://ankiweb.net/shared/info/457099967).
2. Just change you own Cloze Template front content with my [front.html](https://github.com/ruin1990/AnkiTemplate/ClozeAdv/front.html).


## Features
1. We can use touch/click/keyboard(Tab and Backquote) to reveal or cover the cloze.(Thanks: [kleinerpirat](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584))
2. If all the clozes are revealed, the card will auto flip to back.(Thanks: [git9527](https://github.com/git9527/anki-awesome-select))
3. I add a float button view for reveal next cloze or cover previous cloze.(Thanks: [kleinerpirat](https://ankiweb.net/shared/info/1231171279))(Support English and Chinese automatically)
4. It can support multi-cloze sperate by c[n], some template will convert all the c[n] to c1
5. Mathjax block is supported NOW!!!

> Demo for Mathjax

![mathjax](https://s2.loli.net/2022/01/18/bMEhgUJaDLcqk8r.gif)

> Demo for reciting Chinese

![demo](https://s3.bmp.ovh/imgs/2021/12/a08a795d540e1a09.gif)

## Bugs
~~ClozeAdv cannot support MathJax formulation cloze or some complex span/div.~~
~~So, I skip the MathJax's convertion.~~  

MathJax is support NOW!!!

## Compatibility
| Platform | Support |
| ---- | ---- |
| AnkiDroid     | **YES** |
|   AnkiMobile   | Problem with iOS layout of floating buttons |
|  AnkiWindows    | **YES** |
|   AnkiMacOS   |  Not test, but I think it's supported   |

I would appreciate it if someone could give feedback on the results of compatibility

## License
Apache License V2.0

## Plus
If you find a bug, please let me know. It's best to bring the card set that repeats the problem

## Thanks & Reference
1. Keyboard support, [kleinerpirat](https://forums.ankiweb.net/t/cloze-one-by-one-uncovering/12584)
2. Auto flip to back, [git9527](https://github.com/git9527/anki-awesome-select)
3. Float button view, [kleinerpirat](https://ankiweb.net/shared/info/1231171279)
