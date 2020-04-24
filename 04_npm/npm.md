## Node 中除了它自己提供的核心模块之外，还可以自定义模块，以及使用 第三方模块。
 Node 中第三方模块由包组成，可以通过包来对一组具有相互依赖关系的模块进行统一管理。

 那么，假如我们需要使用一些第三方模块，应该去哪找呢？

1. 百度。百度查找你需要安装的第三方模块的对应内容。
2. npm 官网。如果你已经知道包的名字或者包的作用。那么，直接在 npm 官网上搜索，想必会更快找到想要安装的包。

那么，npm 是啥

npm 是世界上最大的开放源代码的生态系统。我们可以通过 npm 下载各种各样的包。 

在我们安装 Node 的时候，它默认会顺带给你安装 npm。

- ``npm -v``：查看 ``npm`` 版本。
- ``npm list``：查看当前目录下都安装了哪些 npm 包。
- ``npm info`` 模块：查看该模块的版本及内容。
- ``npm i`` 模块@版本号：安装该模块的指定版本。

 在平时使用 npm 安装包的过程中，你可能需要知道一些 npm 基本知识：

- ``i/install``：安装。使用 ``install`` 或者它的简写 ``i``，都表明你想要下载这个包。
- ``uninstall``：卸载。如果你发现这个模块你已经不使用了，那么可以通过 ``uninstall`` 卸载它。
- ``g``：全局安装。表明这个包将安装到你的计算机中，你可以在计算机任何一个位置使用它。
- ``--save/-S``：通过该种方式安装的包的名称及版本号会出现在 ``package.json`` 中的 ``dependencies`` 中。``dependencies`` 是需要发布在生成环境的。例如：``ElementUI`` 是部署后还需要的，所以通过 ``-S`` 形式来安装。
- ``--save-dev/-D``：通过该种方式安装的包的名称及版本号会出现在 ``package.json`` 中的 ``devDependencies`` 中。``devDependencies`` 只在开发环境使用。例如：``gulp`` 只是用来压缩代码、打包的工具，程序运行时并不需要，所以通过 ``-D`` 形式来安装。

 例子：

- ``cnpm i webpack-cli -D``
- ``npm install element-ui -S``

 那么，这么多的 npm 包，我们通过什么管理呢？

答案是 ``package.json``。

如果我们需要创建 ``package.json``，那么我们只需要在指定的包管理目录（例如 ``node_modules``）中通过以下命名进行生成：

- ``npm init``：按步骤创建 ``package.json``。
- ``npm init --yes``：快速创建 ``package.json``

 当然，因为国内网络环境的原因，有些时候通过 npm 下载包，可能会很慢或者直接卡断，这时候就要安装淘宝的 ``npm`` 镜像：``cnpm``

``npm install -g cnpm --registry=https://registry.npm.taobao.org``
