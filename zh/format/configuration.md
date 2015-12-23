# 配置

所有的配置信息都以 JSON 的形式写在 `book.json` 文件中.

你可以将你 `book.json` 文件中的 JSON 粘贴到网站 [jsonlint.com](http://jsonlint.com) 来验证 JSON 的格式是否正确.

所有的子段都是可选的或者存在默认值.


## 字段

#### gitbook

```js
{ "gitbook": "2.x.x" }
```

此选项用于检测将使用哪个版本的 GitBook 来生成书.格式符合 [SEMVER](http://semver.org) 规范.

#### title

```js
{ "title": "My Awesome Book" }
```

这个选项定义你书籍的标题, 默认情况下该值从 **README** 读取(第一个标题)。

在网站 **gitbook.com**, this value is defined from the title entered on the platform.

#### description

```js
{ "description": "This is such a great book!" }
```

这个选项定义你书籍的描述信息, 默认情况下该值从 **README** 读取(第一段).

在网站 **gitbook.com**, this value is defined from the description entered on the platform.

#### isbn

```js
{ "isbn": "978-3-16-148410-0" }
```

这个选项定义你书籍的 ISBN（国际标准书号).  

#### language

```js
{ "language": "fr" }
```

这个选项定义书籍的语言, 默认值是 `en`.

此选项用于国际化和本地化, 它会改变网站的内容。

在网站 **gitbook.com**, this value is defined from the language detected in the content or specified in the settings.

#### direction

```js
{ "direction": "rtl" }
```

This option is used to override the text direction from the language.
It is recommended to set the `language` field to a language with the correct text direction instead.

#### styles

This option is used to add custom css to your book.

Example:

```js
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}
```

#### plugins

```js
{ "plugins": ["mathjax"] }
```

The list of plugins being used by a book is defined in the `book.json` configuration.

#### pluginsConfig

```js
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

This option contains all plugins specific configurations.

#### structure

This option is used to override files paths used by GitBook.

For example if you want to use `INTRO.md` instead of `README.md`:

```js
{
    "structure": {
        "readme": "INTRO.md"
    }
}
```

Structure types are `readme`, `langs`, `summary` and `glossary`.

#### variables

```js
{
    "variables": {
        "myTest": "Hello World"
    }
}
```

This option defines the variables values being used in [templating](./templating.md).

#### pdf

PDF specific options allow customization of header, footer, etc

```js
{
    "pdf": {
        "headerTemplate": "Header of the PDF with _TITLE_",
        "footerTemplate": "Footer HTML template. Available variables: _PAGENUM_, _TITLE_, _AUTHOR_ and _SECTION_."
    }
}
```
