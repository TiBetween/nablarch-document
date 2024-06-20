# nablarch-document
这是Nablarch开源项目的文档。

## 前提
本文档使用Sphinx构建。

## 构建环境
建议使用Windows或Docker进行构建。
### Windows
#### 文档构建环境
安装Python 3.6.x 及以下版本的插件。
* Sphinx(1.6.3)
* javasphinx(0.9.15)
* sphinx-rtd-theme(0.2.4)
#### textlint运行环境
除上述内容外，还需安装以下内容：
* Node.js（已确认在v16.16.0上可运行）
* 使用npm安装依赖库。
  ```sh
  npm install
  ```
* 需要安装docutils-ast-writer，这是[textlint-plugin-rst](https://github.com/jimo1001/textlint-plugin-rst)的依赖库。
  ```sh
  pip install docutils-ast-writer
  ```
#### linkcheck运行环境
与文档构建环境相同。

### Docker
#### 文档构建、textlint和linkcheck运行环境
请使用以下命令构建映像。
```
docker build -t nablarch-document-build .
```
##### (附加信息)已确认可运行的Docker主机
- WSL2 + Windows上的Docker Desktop
- 无需代理

## 文档构建方法
### Windows
* 日语文档
  ```bash
  make html ja
  ```
* 英语文档
  ```bash
  make html en
  ```

### Docker
* 日语文档
  ```bash
  docker run --rm -v <克隆存储库的完整路径>:/root/document nablarch-document-build /bin/bash -c "cd /root/document; sphinx-build -d _build/.doctrees/ja -b html ja _build/html"
  ```
* 英语文档
  ```bash
  docker run --rm -v <克隆存储库的完整路径>:/root/document nablarch-document-build /bin/bash -c "cd /root/document; sphinx-build -d _build/.doctrees/en -b html en _build/html/en"
  ```

## textlint运行方法
### textlint配置文件
使用以下配置文件。无需编辑。

  | 文件                   | 描述           |
  |------------------------|----------------|
  | .textlintrc            | textlint配置   |
  | .textlint/conf/prh.yml | 词典           |

### 通信确认
#### Windows
* 日语文档
  ```sh
  ./node_modules/.bin/textlint .textlint/test/test.rst
  ```
  如果将`./node_modules/.bin`添加到PATH中，可以简化为以下方式运行：
  ```sh
  textlint .textlint/test/test.rst
  ```

#### Docker
* 日语文档
  ```sh
  docker run --rm -v <克隆存储库的完整路径>:/root/document nablarch-document-build /bin/bash -c "cd /root/document; ../node_modules/.bin/textlint .textlint/test/test.rst"
  ```

### 执行
#### Windows
* 指定目标目录以运行textlint。
  ```sh
  ./node_modules/.bin/textlint ja/development_tools
  ```

#### Docker
* 指定目标目录以运行textlint。
  ```sh
  docker run --rm -v <克隆存储库的完整路径>:/root/document nablarch-document-build /bin/bash -c "cd /root/document; ../node_modules/.bin/textlint ja/development_tools"
  ```

## linkcheck运行方法
### 运行
#### Docker
* 日语文档
  ```bash
  docker run --rm -v <克隆存储库的完整路径>:/root/document nablarch-document-build /bin/bash -c "cd /root/document; sphinx-build -d _build/.doctrees/ja -b linkcheck ja _build/linkcheck/ja"
  ```

* 英语文档
  ```bash
  docker run --rm -v <克隆存储库的完整路径>:/root/document nablarch-document-build /bin/bash -c "cd /root/document; sphinx-build -d _build/.doctrees/en -b linkcheck en _build/linkcheck/en"
  ```