## 介绍

### PhyloScape是什么

[PhyloScape](http://www.phyloscape.cc/) 是一款基于 [d3.js](https://d3js.org/) 的用于可视化系统进化树的插件（以下简称“本插件”），支持 tree 、radial 布局、 支持导入导出 `Newick` 、 `NEXUS` 、`NeXML`、`Phyloxml`等格式的树文件，且具备选中分支、编辑子树、添加子树、进化分支优化、树结构转换、字体切换、元数据展示、保存所选枝叶、重置树、将进化树图像导出为 `SVG` 、 `PNG` 等功能。

### 快速安装

#### CDN 引入

在页面上引入[PhyloScape](http://www.phyloscape.cc/cdn/phyloscape.js)。最新版支持 `CommonJS` 以及基础标签引入形式，对于生产环境，我们推荐链接到一个明确的版本号和构建文件，以避免新版本造成的不可预期的破坏。（建议下载 [PhyloScape](http://www.phyloscape.cc/cdn/phyloscape.js) 在本地引入）

```html
<!-- 在线引入PhyloScape -->
<script src="http://www.phyloscape.cc/cdn/phyloscape.main.js"></script>
```

**示例展示**

通过 CDN 可以快速使用 [PhyloScape](http://www.phyloscape.cc/cdn/phyloscape.js) 写出一个 `tree` 示例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>phyloscape</title>
</head>

<body>
    <div id="dendrogram"></div>
    <script src="http://www.phyloscape.cc/cdn/phyloscape.main.js"></script>
    <script>
        new phyloscape.InitTreeStructure("#dendrogram", { content: "" })
        // 或者
        phyloscape.InitTreeLayoutStructure("#dendrogram", {
            content: "",
            layout: "tree"
        })
    </script>
</body>

</html>
```

通过 CDN 可以快速使用 [PhyloScape](http://www.phyloscape.cc/cdn/phyloscape.js) 写出一个 `radial` 示例：
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>phyloscape</title>
</head>

<body>
    <div id="dendrogram"></div>
    <script src="http://www.phyloscape.cc/cdn/phyloscape.main.js"></script>
    <script>
        new phyloscape.InitRadialStructure("#dendrogram", { content: "" })
        // 或者
        phyloscape.InitTreeLayoutStructure("#dendrogram", {
            content: ""
            layout: "radial"
        })
    </script>
</body>

</html>
```

#### NPM 安装

##### phyloscape
推荐使用 `npm` 来安装，享受生态圈和工具带来的便利，更好地和 `webpack` 配合使用，当然，我们也推荐使用 `ES2015`。

```js
import phyloscape from "phyloscape";

new phyloscape.InitTreeStructure("#dendrogram", { content: "" })

// 或者
new phyloscape.InitRadialStructure("#dendrogram", { content: "" })

// 或者
phyloscape.InitTreeLayoutStructure("#dendrogram", {
    content: ""
    layout: "" // radial、tree
})
```
##### NPM 按需引用

```js
import { InitTreeStructure, InitRadialStructure, InitTreeLayoutStructure } from "phyloscape";

new InitTreeStructure("#dendrogram", { content: "" })

// 或者
new InitRadialStructure("#dendrogram", { content: "" })

// 或者
InitTreeLayoutStructure("#dendrogram", {
    content: ""
    layout: "" // radial、tree
})
```

#### 支持的环境

`PhyloScape` 支持最新浏览器，比如 `Chrome`，`Edge`，`Firefox` 以及 `Safari`。