.. フロントエンドとバックエンドの分離 documentation master file, created by
   sphinx-quickstart on Fri Jun 12 15:11:35 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

フロントエンドとバックエンドの分離
==============================================================

認証なしフロー例
--------------------------------------------------------------

.. seqdiag::
   :desctable:

   seqdiag {
      browsers -> frontend_server [label = "GET /article"];
          frontend_server -> backend_server [label = "GET /api/v1/article"];
          frontend_server <-- backend_server [label = "article list json data"];

          frontend_server -> backend_server [label = "GET /api/v1/notice"];
	  frontend_server <-- backend_server [label = "notice list json data"];

      browsers <- frontend_server

      browsers [description = "browsers in each client"];
      frontend_server [description = "node.js/Vue"];
      backend_server [description = "nginx/PHP"];
   }


認証フロー
--------------------------------------------------------------

.. seqdiag::
   :desctable:

   seqdiag {
      browsers -> frontend_server [label = "GET /signin"];
      browsers <-- frontend_server

      browsers -> frontend_server [label = "POST /signin"];
          frontend_server -> backend_server [label = "POST /api/v1/token"];
          frontend_server <-- backend_server [label = "token json data"];

      browsers <- frontend_server [label = "token json data"];

      browsers [description = "browsers in each client"];
      frontend_server [description = "node.js/Vue"];
      backend_server [description = "nginx/PHP"];
   }


.. toctree::
   :maxdepth: 2
   :caption: Contents:



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
