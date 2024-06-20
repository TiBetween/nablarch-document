
.. image:: ./_image/Nablarch.jpg
 :width: 300px

.. raw:: html

  <div id="top-logo">&nbsp;</div>

=======================
Nablarch
=======================

.. toctree::
  :maxdepth: 1
  :hidden:


  about_nablarch/index
  application_framework/index
  extension_components/index
  development_tools/index
  examples/index
  nablarch_api/index
  releases/index
  about_nablarch/versionup_policy
  inquiry/index
  terms_of_use/index

-----------------------------------------------
关于Nablarch
-----------------------------------------------


Nablarch是由TIS丰富的核心系统构建经验积累而成的Java应用开发/执行基础设施。


 | :doc:`概念 <about_nablarch/concept>`
 | :doc:`许可证 <about_nablarch/license>`


-----------------------------------------------
Nablarch系统开发指南
-----------------------------------------------

针对使用Nablarch进行系统开发的程序员，在开发开始之前·开发过程中应该做些什么的指南。

 | `系统开发指南 <https://fintan.jp/page/252/>`__

-----------------------------------------------
Nablarch开发标准
-----------------------------------------------

设计书和代码编写是应该遵循的准则。

 | `开发标准 <https://fintan.jp/page/1868/#development-standards>`__


-----------------------------------------------
Nablarch应用程序框架
-----------------------------------------------

  | :doc:`模块一览 <about_nablarch/mvn_module>`
  | :doc:`说明书 <application_framework/application_framework/index>`
  | :doc:`适配器 <application_framework/adaptors/index>`
  | :doc:`示例 <application_framework/example/index>`
  | :doc:`云原生支持 <application_framework/application_framework/cloud_native/index>`

-----------------------------------------------
Nablarch扩展组件
-----------------------------------------------

帳票 [#form]_ 库
===========================

  | :doc:`说明书 <extension_components/report/index>` | `示例应用程序 <https://github.com/nablarch/nablarch-report-sample>`__
  
工作流库
===========================

  | :doc:`说明书 <extension_components/workflow/doc/index>`
  | :doc:`工作流定义数据自动生成工具 <extension_components/workflow/tool/index>` |

ETL平台
===========================

  | :doc:`说明书 <extension_components/etl/index>`
  | :doc:`ETL Maven Plugin <extension_components/etl/etl_maven_plugin>`


-----------------------------------------------
Nablarch开发工具
-----------------------------------------------

高效的代码静态检查
===========================

  | :doc:`说明书 <development_tools/java_static_analysis/index>` 

为高级前端开发人员准备的的UI开发平台
====================================

  | :doc:`说明书 <development_tools/ui_dev/index>` | :doc:`JSP/HTML编写指南 <development_tools/ui_dev/guide/index>` 


测试框架
==============================================

  | :doc:`说明书 <development_tools/testing_framework/index>` | :doc:`模块一览 <about_nablarch/mvn_module>`


应用程序开发时可以使用的方便的工具
==========================================

  | :doc:`说明书 <development_tools/toolbox/index>` 


-----------------------------------------------
Nablarch开发示例
-----------------------------------------------

  | :doc:`说明书 <examples/index>`


-----------------------------------------------
relase信息
-----------------------------------------------

  | :doc:`relase note <releases/index>`


-----------------------------------------------
特性新增需求・改进需求
-----------------------------------------------

  | :doc:`特性新增需求・改进需求 <inquiry/index>`

.. [#form] 
    考虑到实际工作中常使用帳票这一概念，此处不进行翻译，其中文对应含义为**账本和票据(发票)类的总称**
    ——译者注