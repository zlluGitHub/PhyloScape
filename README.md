# PhyloScape documentation

## Introduction

### About PhyloScape JS library

[PhyloScape](http://www.phyloscape.cc) JS library is based on [d3.js](https://d3js.org) for visualizing Phylogenetic trees. PhyloScape supports tree files in Newick and Nexus formats and exports images in SVG and PNG formats. Additionally, PhyloScape features branch selection, subtree editing, subtree addition, optimization of evolutionary branches, tree structure conversion, font switching, metadata display, saving selected branches and leaves, and resetting the tree.

### Quick Use

#### CDN install

The lastest version of PhyloScape library now supports `CommonJS` and introducing with the basic label. We recommend linking to a specific version to prevent unexpected disruption. It is advisable to download PhyloScape for local implementation.

```html
<!-- import PhyloScape online -->
<script src="http://www.darwintree.cn/PhyloScape/phyloscape.main.js"></script>
```

Examples

A tree example can be quickly created using PhyloScape via a CDN:

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
    <script src="http://www.darwintree.cn/PhyloScape/phyloscape.main.js"></script>
    <script>
        new phyloscape.InitTreeStructure("#dendrogram", { content: "" })
        // or
        phyloscape.InitTreeLayoutStructure("#dendrogram", {
            content: "",
            layout: "tree"
        })
    </script>
</body>

</html>
```

A `radial` example can be quickly created using PhyloScape via a CDN:
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
    <script src="http://www.darwintree.cn/PhyloScape/phyloscape.main.js"></script>
    <script>
        new phyloscape.InitRadialStructure("#dendrogram", { content: "" })
        // or
        phyloscape.InitTreeLayoutStructure("#dendrogram", {
            content: ""
            layout: "radial"
        })
    </script>
</body>

</html>
```

#### NPM install

use npm

We recommend installing via npm to enjoy the convenience brought by the ecosystem and tools, and to better integrate with webpack.

example

```javascript
import phyloscape from "phyloscape";

new phyloscape.InitTreeStructure("#dendrogram", { content: "" })

// or
new phyloscape.InitRadialStructure("#dendrogram", { content: "" })

// or
phyloscape.InitTreeLayoutStructure("#dendrogram", {
    content: ""
    layout: "" // radial、tree
})
```

NPM on-demand import
```javascript
import { InitTreeStructure, InitRadialStructure, InitTreeLayoutStructure } from "phyloscape";

new InitTreeStructure("#dendrogram", { content: "" })

// or
new InitRadialStructure("#dendrogram", { content: "" })

// or
InitTreeLayoutStructure("#dendrogram", {
    content: ""
    layout: "" // radial、tree
})
```

#### Supported Environments

PhyloScape is compatible with the latest versions of all major browsers, including Chrome, Edge, Firefox, and Safari.

