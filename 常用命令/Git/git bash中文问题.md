你要执行的是这个：

```bash
git config --global core.quotepath false
```

拆开翻译：

```bash
git
```

意思：调用 Git 这个工具。

```bash
config
```

意思：修改/查看 Git 的配置。

```bash
--global
```

意思：全局配置。也就是你电脑上以后所有 Git 项目都按这个设置来，不只是当前这个项目。

```bash
core.quotepath
```

意思：Git 显示文件路径时，要不要把非英文字符转义。

比如中文文件名：

```bash
今天.md
```

Git 默认可能显示成：

```bash
\344\273\212\345\244\251.md
```

这就是你截图里的那种鬼东西。

```bash
false
```

意思：关闭这个转义。

所以整句意思就是：

> 让 Git 以后显示中文文件名时，直接显示中文，不要显示成一堆 `\344\273...` 这种编码。

执行完之后，再执行：

```bash
git status
```

意思是：

> 查看当前项目的 Git 状态，比如哪些文件改了、有没有提交、当前在哪个分支。

你也可以只对当前项目生效，用这个：

```bash
git config core.quotepath false
```

区别是少了 `--global`：

```bash
git config core.quotepath false
```

意思：

> 只让当前这个项目显示中文路径，不影响其他项目。

我建议你直接执行这个就行：

```bash
git config --global core.quotepath false
git status
```

安全的，不会改你的代码，也不会提交文件，只是改 Git 的显示方式。