.. The contents of this file are included in multiple topics.
.. THIS FILE SHOULD NOT BE MODIFIED VIA A PULL REQUEST.

This configuration file has the following settings for ``opscode-certificate``:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_certificate['dir']``
     - |directory generic| |default_value_recommended| Default value: ``"/var/opt/opscode/opscode-certificate"``.
   * - ``opscode_certificate['enable']``
     - |enable service| Default value: ``true``.
   * - ``opscode_certificate['ha']``
     - |use ha| Default value: ``false``.
   * - ``opscode_certificate['log_directory']``
     - |directory logs| |default_value_recommended| Default value: ``"/var/log/opscode/opscode-certificate"``.
   * - ``opscode_certificate['log_rotation']``
     - |log_rotation| Default value: ``{ 'file_maxbytes' => 104857600, 'num_to_keep' => 10 }``
   * - ``opscode_certificate['num_certificates_per_worker']``
     - The number of certificates for each allowed worker processes. Default value: ``"50"``.
   * - ``opscode_certificate['num_workers']``
     - The number of allowed worker processes. Default value: ``"2"``.
   * - ``opscode_certificate['port']``
     - |port service| Default value: ``5140``.
   * - ``opscode_certificate['vip']``
     - |ip_address virtual| Default value: ``"127.0.0.1"``.