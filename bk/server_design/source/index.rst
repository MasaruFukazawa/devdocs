.. サーバ設計書 documentation master file, created by
   sphinx-quickstart on Tue Jan 14 12:04:59 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

サーバ設計書
========================================


サーバ概念図
----------------------------------------


サーバ構成図
----------------------------------------

セキュリティグループ
----------------------------------------

**WEBサーバSG**

.. list-table::
   :header-rows: 1

   * - インバウンド/アウトバウンド
     - タイプ
     - プロトコル
     - ポート範囲
     - 送信先
   * - インバウンド
     - SSH
     - TCP
     - 22
     - 000.111.222.333

       
IAMユーザ
----------------------------------------


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
