.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.

This configuration file has the following settings for ``opscode-solr4``:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_solr4['auto_soft_commit']``
     - The maximum number of documents before a soft commit is triggered. Default value: ``1000``.
   * - ``opscode_solr4['commit_interval']``
     - |solr_commit_interval| This value should be tuned carefully. |solr_update_frequency_caveat| Default value: ``60000`` (every 60 seconds).
   * - ``opscode_solr4['data_dir']``
     - |directory generic_data| |default_value_recommended| Default value: ``/var/opt/chef-server/chef-solr/data``.
   * - ``opscode_solr4['dir']``
     - |directory generic| |default_value_recommended| Default value: ``/var/opt/chef-server/chef-solr``.
   * - ``opscode_solr4['enable']``
     - |enable service| Default value: ``true``.
   * - ``opscode_solr4['ha']``
     - |use ha| Default value: ``false``.
   * - ``opscode_solr4['heap_size']``
     - |heap_size solr| The default value should work for many organizations with fewer than 25 nodes. For an organization with several hundred nodes, the amount of memory that is required often exceeds 3GB. Default value: ``nil``, which is equivalent to 25% of the system memory or 1024 (MB, but this setting is specified as an integer number of MB in EC11), whichever is smaller.
   * - ``opscode_solr4['ip_address']``
     - The IP address for the machine on which |apache solr| is running. Default value: ``127.0.0.1``.
   * - ``opscode_solr4['java_opts']``
     - A |ruby hash| of ``JAVA_OPTS`` environment variables to be set. (``-XX:NewSize`` is configured using the ``new_size`` setting.) Default value: ``(empty)``.
   * - ``opscode_solr4['log_directory']``
     - |directory logs| |default_value_recommended| Default value: ``/var/log/chef-server/chef-solr``.
   * - ``opscode_solr4['log_rotation']``
     - |log_rotation| Default value: ``{ 'file_maxbytes' => 104857600, 'num_to_keep' => 10 }``
   * - ``opscode_solr4['max_commit_docs']``
     - |solr_max_commit_docs| This value should be tuned carefully.  |solr_update_frequency_caveat| Default value: ``1000`` (every 1000 documents).
   * - ``opscode_solr4['max_field_length']``
     - |solr_max_field_length| Default value: ``100000`` (increased from the |apache solr| default value of ``10000``).
   * - ``opscode_solr4['max_merge_docs']``
     - The maximum number of index segments allowed before they are merged into a single index. Default value: ``2147483647``.
   * - ``opscode_solr4['merge_factor']``
     - The maximum number of document updates that can be stored in memory before being flushed and added to the current index segment. Default value: ``100``.
   * - ``opscode_solr4['new_size']``
     - Use to configure the ``-XX:NewSize`` ``JAVA_OPTS`` environment variable. Default value: ``nil``.
   * - ``opscode_solr4['poll_seconds']``
     - The frequency (in seconds) at which the secondary machine polls the primary. Default value: ``20``.
   * - ``opscode_solr4['port']``
     - |port service| Default value: ``8983``.
   * - ``opscode_solr4['ram_buffer_size']``
     - The size (in megabytes) of the RAM buffer. When document updates exceed this amout, pending updates will be flushed. Default value: ``200``.
   * - ``opscode_solr4['url']``
     - Default value: ``"http://localhost:8983"``.
   * - ``opscode_solr4['vip']``
     - |ip_address virtual| Default value: ``127.0.0.1``.
