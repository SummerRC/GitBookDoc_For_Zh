# Markdown

GitBook 默认使用 Markdown 的语法 .

这是作为一个快速的参考和展示 . 更多详细信息见 [John Gruber's original spec](http://daringfireball.net/projects/markdown/) 和 [Github-flavored Markdown info page](http://github.github.com/github-flavored-markdown/) .


## 标题

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

另外，对一级标题和二级标题，下划线的样式：

```markdown
Alt-H1
======

Alt-H2
------
```

## 段落和换行符

一个段落是一个或多个连续的文本行，由一个或多个空白行分隔。 (这些空白行都视为一个空白行 —— 一行只包括空格或者制表符被认为是空白的 .) 正常的段落不应留有空格或制表符 .

```markdown
从这里开始一行.

这一行从上面开始被两个换行分开, 因此它是一个 *单独的段落*.

这一行也是一个单独的段落, 但是...
这一行只被一个单独的换行分开，因此它时 *同一段落* 的新一行 .
```


## 强调

```markdown
强调, 又名斜体, 用 *星号* 或者 _下划线_ .

特别强调, 又称加粗, 用 **两个星号** 或者 __两个下划线__ .

两者结合可以用 **两个星号 和 _一个下划线_** .

删除线使用两个 `~` 符号. ~~删除这个~~
```

## 列表

(在这个例子中，首尾空格用点表示: ⋅)

```markdown
1. 列表第一项
2. 另一项
⋅⋅* 无序子列表
1. 实际数字并不重要,只是一个编号
⋅⋅1. 有序子列表
4. 另一项

⋅⋅⋅你可以在列表项中适当缩进段落 . 注意上面的空行和空格 (至少有一个空行，但我们也可以在这里使用三个点达到同样的效果) .

⋅⋅⋅新起一行而不新起一段, 你需要在上一行后面空两格然后回车 .⋅⋅
⋅⋅⋅注意这一行是新起的一行，但是和上一行在相同段落里 .⋅⋅
⋅⋅⋅(这与典型的 GFM 换行符不同， 它的行后面不需要两个空格 .)

* 无序列表可以使用星号
- 或者减号
+ 或者加号
```

## 链接

有两种方式创建链接 .

```markdown
[我是一个行内式的链接](https://www.google.com)

[我是一个有标题的行内式的链接](https://www.google.com "Google's Homepage")

[我是一个参考式的链接][任意的不区分大小写的参考文本]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself]

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
```

## Footnotes
The default footnote-style links that Markdown uses do not display on the page. Sometimes it is useful to include a non-hyperlink footnote that will be visible to the reader. GitBook supports a simple syntax for such footnotes.

```markdown
Text prior to footnote reference.[^2]
[^2] Comment to include in footnote.
```

## Images

```markdown
Here's our logo (hover to see the title text):

Inline-style:
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style:
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"
```

## Code and Syntax Highlighting

Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and *Markdown Here* -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer. *Markdown Here* supports highlighting for dozens of languages (and not-really-languages, like diffs and HTTP headers); to see the complete list, and how to write the language names, see the [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html).

```markdown
Inline `code` has `back-ticks around` it.
```

Blocks of code are either fenced by lines with three back-ticks <code>```</code>, or are indented with four spaces. I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.

<pre lang="no-highlight"><code>```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```
No language indicated, so no syntax highlighting.
But let's throw in a &lt;b&gt;tag&lt;/b&gt;.
```
</code></pre>

## Tables

Tables aren't part of the core Markdown spec, but they are part of GFM and *Markdown Here* supports them. They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.

```markdown
Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

## Blockquotes

```markdown
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

## Inline HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well.

```markdown
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```


## Horizontal Rule

```markdown
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

