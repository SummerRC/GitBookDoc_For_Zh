# 模板

这是 GitBook 可用的模板功能的预览. GitBook 使用 [Nunjucks](https://mozilla.github.io/nunjucks/) 和 [Jinja2](http://jinja.pocoo.org/) 两个模板引擎的语法.

### 转义

如果你想输出一些特殊的模板标签, 你可以使用原生的并且任何转义包含的内容都会被当作纯文本输出.

```
{% raw %}
  this will {{ not be processed }}
{% endraw %}
```

### 变量

A variable looks up a value from the book context.

变量被定义在 `book.json` 文件中:

```json
{
    "variables": {
        "myVariable": "Hello World"
    }
}
```


#### 显示变量

Variables specified in the `book.json` are accessible under the scope `book`:

```
{{ book.myVariable }}
```

This looks up `myVariable` from the book variables and displays it. Variable names can have dots in them which lookup properties. You can also use the square bracket syntax.

```
{{ book.foo.bar }}
{{ book["bar"] }}
```

If a value is undefined, nothing is displayed. The following all output nothing if `foo` is undefined: `{{ foo }}`, `{{ foo.bar }}`, `{{ foo.bar.baz }}`.


#### Context variables

Some variables are also available to get informations about the current file or the GitBook instance:

| Name | Description |
| ---- | ----------- |
| `file.path` | Path of the file relative to the book |
| `file.mtime` |Last modified date of the file |


### Tags

Tags are special blocks that perform operations on sections of the template.

#### If

**if** tests a condition and lets you selectively display content. It behaves exactly as a programming language's if behaves.

````
{% if variable %}
  It is true
{% endif %}
```

If `variable` is defined and evaluates to true, "It is true" will be displayed. Otherwise, nothing will be.

You can specify alternate conditions with elif and else:

```
{% if hungry %}
  I am hungry
{% elif tired %}
  I am tired
{% else %}
  I am good!
{% endif %}
```

#### for

**for** iterates over arrays and dictionaries.

Let's consider your variables in the `book.json`:
```
{
    "variables": {
        "authors": [
            { "name": "Samy" },
            { "name": "Aaron" }
        ]
    }
}
```

```
# Authors


{% for author in book.authors %}
  - {{ author.name }}
{% endfor %}
```

The above example lists all the authors using the `name` attribute of each item in the `authors` array as the display value.

#### include

Include is detailed in the [Content References](./conrefs.md) article.
