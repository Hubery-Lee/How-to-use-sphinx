
如何使用
============

该手册采用`reStructuredText <http://docutils.sourceforge.net/rst.html>`_标记语言撰写, 使用Sphinx进行发布.


+----------+----------------------------------------------------------------+
| 属性     | 值                                                             |
+==========+================================================================+
| 开发语言 | `reStructuredText <http://docutils.sourceforge.net/rst.html>`_ |
+----------+----------------------------------------------------------------+
| 发布工具 | `Sphinx <http://www.sphinx-doc.org/en/stable/>`_               |
+----------+----------------------------------------------------------------+


快速入门
---------------
`Quick reStructuredText <https://docutils.sourceforge.io/docs/user/rst/quickref.html#field-lists>`_

行内markup
++++++++++++++++

.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-08%20232949.png


结构化
++++++++++++++++
.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-08%20233847.png

列表
++++++++++++++++
项目符号列表、数字枚举列表与markdown语法一样

.. tip::

    域列表和选项列表 markdown语法没有

.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-08%20234301.png

文字块
+++++++++++++++

.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-08%20234908.png


竖线块
+++++++++++++++

.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-08%20235107.png


超链接目标
+++++++++++++++

外部超链接，内部超链接

.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-08%20235942.png

图片的直接使用与替代参考与定义
++++++++++++++++++++++++++++++

.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-09%20000253.png


参考资料
++++++++++
.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-09%20001417.png

表格
+++++++
.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-09%20001646.png


注释
+++++++
.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-09%20001800.png


脚注
++++++++++
.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-09%20001321.png

评论
++++++++++++
.. image:: https://gitee.com/hubery_lee123/image-source/raw/master/Screenshot%202021-02-09%20000856.png


代码块
++++++++++
.. code-block:: restructedtext

    .. math::
    α_t(i) = P(O_1, O_2, … O_t, q_t = S_i λ)

测试代码
++++++++++

>>>print('this is my test')

数学公式
+++++++++

采用latex风格的数学输入

.. code-block:: restructedtext

    .. math::
    α_t(i) = P(O_1, O_2, … O_t, q_t = S_i λ)

.. math::

  α_t(i) = P(O_1, O_2, … O_t, q_t = S_i λ)


一些特殊块的使用
+++++++++++++++++

`caution、danger、error、hint、important、note、tip、warning、admonition`

详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. caution:: 

    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. danger:: 

    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. error:: 

    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. hint:: 
    
    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. important:: 
    
    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. note:: 

    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. tip:: 
    
    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. warning:: 
    
    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_

.. admonition:: 
    
    详细入门资料请查看 `restructuredtext <https://docutils.sourceforge.io/docs/ref/rst/directives.html>`_


如何部署
=============

采用github 登入readthedoc，授权后，导入托管参考即可

如何转换成pdf
===============
用sphinx写好的文档可以转成pdf格式，以前不是说自己要写一本书么，现在就可以实现了，而且都是可以按照自己的风格来排版，到时候自己出钱就可以出书了，是不是感觉特别棒。

pip nstall rst2pdf

Add rst2pdf to the list of extensions in conf.py
extensions = ['rst2pdf.pdfbuilder']

This list will be empty if you accepted the defaults when the project was setup. If not, just append ‘rst2pdf.pdfbuilder’ to the list.

Add a pdf_documents variable to conf.py

.. code-block:: 

    pdf_documents = [('index', u'rst2pdf', u'Sample rst2pdf doc', u'Your Name'),]

    # rst2pdf - name of the generated pdf
    # Sample rst2pdf doc - title of the pdf
    # Your Name - author name in the pdf

Generate pdf
.. code-block:: 
    
    make pdf

The generated pdf will be in the build/pdf directory.

https://www.dazhuanlan.com/2019/10/06/5d99f684a0c43/

中文乱码解决办法
----------------

https://www.tutorialfor.com/blog-222028.htm
