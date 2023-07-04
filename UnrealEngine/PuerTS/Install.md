# Install PuerTS

## 安装PuerTS插件

前置：需要一个已有的Unreal Cpp工程项目

参考官方文档：
Clone PuerTS GitHub项目，
选择某一个发布版本的tag(比如Unreal_v1.0.4)，git checkout tags/Unreal_v1.0.4
然后拷贝到项目中的Plugins目录
再下载Build好的官方v8版本，注意，解压后的文件夹名字，一定要是v8(不带版本号)
[安装 PuerTS](https://puerts.github.io/docs/puerts/unreal/install)

## 新增调用JS代码的入口

参考[puerts_unreal_demo的TsGameInstace](https://github.com/chexiongsheng/puerts_unreal_demo/blob/master/Source/puerts_unreal_demo/TsGameInstance.cpp)，在项目中，增加一个继承自UGameInstance的类，并且在项目设置中，将默认的GameInstance，改为这个新建的类

项目的Build.cs中，也需要依赖JsEnv模块

## 新增TS代码

## 从零开始新建TS项目(不推荐这种方式)

不推荐的原因是，按照官方文档[typesceript版本升级](https://puerts.github.io/docs/puerts/unreal/faq#typesceript%E7%89%88%E6%9C%AC%E5%8D%87%E7%BA%A7)的说法，开启继承ue类后，支持的typescript版本不高于4.8.3

而下面列的方法，会设置使用最新版本的TypeScript

### 安装NodeJS

去[NodeJS官网](https://nodejs.org/en)下载安装一个LTS版本

下面几步参考了这篇文章
[fastest-way-to-start-a-typescript-project](https://www.mailslurp.com/blog/fastest-way-to-start-a-typescript-project/)

### npm init --yes

在项目根目录下，执行npm init --yes，生成package.json文件

### npm i -D typescript ts-node

然后执行npm i -D typescript ts-node，安装typescript和ts-node，安装完毕之后，会在项目根目录下生成node_modules目录

### .\node_modules\.bin\tsc.cmd --init

在Windows下面，执行.\node_modules\.bin\tsc.cmd --init，生成tsconfig.json文件
