# 说明和介绍

书籍的第一页展示`README.md`文件的内容. If the file is not present in the `SUMMARY`, it will be added as a first entry.

### 使用其他文件替代 README.md

有些托管在GitHub上的书籍更喜欢保持 README.md 作为项目的介绍而不是书籍的介绍.

从 GitBook `2.0.0` 之后的版本开始, 我们可以在 `book.json` 文件中定义任意文件来作为书籍的介绍文件代替 README.md :

```js
{
    "structure": {
        "readme": "myIntro.md"
    }
}
```

**注意:** 介绍文件应该在你书籍的根目录下.