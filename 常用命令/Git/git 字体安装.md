## 1. 安装 Roboto Mono 字体

下载到字体文件后，一般是 `.ttf` 文件，比如：

```
RobotoMono-Regular.ttfRobotoMono-Bold.ttfRobotoMono-Italic.ttf
```

安装方法：

右键字体文件 → **为所有用户安装**

或者：

Windows 设置 → 个性化 → 字体 → 把 `.ttf` 文件拖进去。

安装完之后，最好**关闭 Git Bash，重新打开**，不然它可能识别不到新字体。

Git Bash 里看不到，不一定是没装。Git Bash 用的是 **mintty** 终端，它的字体选择列表会筛选字体；有些字体虽然 Windows 能看到，但 mintty 菜单里不显示。mintty 官方说明也提到：没出现在菜单里的字体，仍然可以通过配置 `Font=` 手动指定。

直接别管那个列表了，手动写配置。

## 你在 Git Bash 执行这个

```
notepad ~/.minttyrc
```

打开后，把下面这几行放进去：

```
Font=Roboto MonoFontHeight=16Charset=UTF-8Locale=zh_CNShowHiddenFonts=true
```

保存，关闭记事本。

然后：**把所有 Git Bash 窗口关掉，重新打开。**

就改好了
