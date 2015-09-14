# Math & TeX

Plugins exist to add math and TeX support to GitBook. There are currently 2 official plugins to display math: [mathjax](https://github.com/GitbookIO/plugin-mathjax) and [katex](https://github.com/GitbookIO/plugin-katex).

#### Enable one of these plugin:

To enable math, you need to add one of these plugin to your `book.json`:

```js
{
    "plugins": ["mathjax"]
}
```

#### Differences between MathJax and KaTeX

These plugins are different on the implementation of the math diaply, there are using two different projects: [KaTeX](https://github.com/Khan/KaTeX) and [MathJax](https://www.mathjax.org).

MathJax support all the TeX syntax, but the output is not perfect on ebooks (PDF, ePub and Mobi).
KaTeX output is perfect on all formats (web and ebooks), but it doesn't support [all the syntax](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX).


#### Add math to your content:

```
Here is some inline math: $$a \ne 0$$
```

Block of math should start with a new line:

```
here is a block of math:

$$
a \ne 0
$$
```