NGINX
=====


Exemple de fichier de configuration Nginx.


.. code-block:: bash

  #/etc/nginx/sites-available/phraseanet.conf
  server {
          listen       80;
          server_name  yourdomain.tld;
          root         /var/www/Phraseanet/www;

          index  index.php;
          include rewrite_rules.inc;

          # PHP scripts -> PHP-FPM server listening on 127.0.0.1:9000
          location ~ \.php(/|$) {
                   fastcgi_pass   127.0.0.1:9000;
                   fastcgi_index  index.php;
                   include fastcgi_params;
                   fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
          }
          location /web {
                  alias /var/www/Phraseanet/datas/web;
          }
  }

.. note:: N'oubliez pas de copier le fichier des règles de re-écriture 
  `rewrite_rules.inc` que vous trouverez dans config/nginx.rewrite.rules


Configuration Auth Token
------------------------

Configuration Pseudo Stream H264
--------------------------------

Configuration XSendFile
-----------------------