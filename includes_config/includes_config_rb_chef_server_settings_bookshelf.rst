.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This configuration file has the following settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``bookshelf['access_key_id']``
     - Default value: ``generated-by-default``.
   * - ``bookshelf['data_dir']``
     - |directory generic_data| |default_value_recommended| Default value: ``/var/opt/chef-server/bookshelf/data``.
   * - ``bookshelf['dir']``
     - |directory generic| |default_value_recommended| Default value: ``/var/opt/chef-server/bookshelf``.
   * - ``bookshelf['enable']``
     - Default value: ``true``.
   * - ``bookshelf['external_url']``
     - The base URL to which the service will return links to API resources. Use ``:host_header`` to ensure the URL is derived from the host header of the incoming HTTP request. Default value: ``:host_header``.
   * - ``bookshelf['ha']``
     - |use ha| Default value: ``false``.
   * - ``bookshelf['listen']``
     - Default value: ``0.0.0.0``.
   * - ``bookshelf['log_directory']``
     - The directory in which log files are located. Default value: ``/var/log/chef-server/bookshelf``.
   * - ``bookshelf['port']``
     - |port service| Default value: ``4321``.
   * - ``bookshelf['secret_access_key']``
     - Default value: ``generated-by-default``.
   * - ``bookshelf['stream_download']``
     - Default value: ``true``.
   * - ``bookshelf['svlogd_num']``
     - |svlogd_num| Default value: ``10``.
   * - ``bookshelf['svlogd_size']``
     - |svlogd_size| Default value: ``1000000``.
   * - ``bookshelf['url']``
     - This value will default to the value of the URL for |nginx|, which is built from the configured ``api_fqdn`` and the SSL port for |nginx|.
   * - ``bookshelf['vip']``
     - Default value: ``node['fqdn']``.