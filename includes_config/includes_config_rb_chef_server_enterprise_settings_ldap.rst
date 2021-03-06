.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The |enterprise rb| file contains the settings required to configure |ldap| or |windows ad|:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``ldap['base_dn']``
     - |ldap base_dn| For |windows ad|, this is typically ``cn=users`` and then the domain. For example: ``'cn=users,dc=opscode,dc=com'``. Default value: ``nil``.
   * - ``ldap['bind_dn']``
     - |ldap bind_dn| This is often the administrator or manager user. This user needs to have read access to all |ldap| users that require authentication. |chef server oec| must do an |ldap| search before any user can log in. Many |windows ad| and |ldap| systems do not allow an anonymous bind. If anonymous bind is allowed, leave the ``bind_dn`` setting blank. If anonymous bind is not allowed, a user with ``READ`` access to the directory is required. This user must be specified as an |ldap| distinguished name similar to ``'cn=user_name,dc=domain_name,dc=com'``. Default value: ``nil``.
   * - ``ldap['bind_password']``
     - |ldap bind_password| Leave this value unset if anonymous bind is sufficient. Default value: ``nil``.
   * - ``ldap['encryption']``
     - Use to specify the encryption method. Possible values: ``:start_tls`` or ``:simple_tls``. Default value: ``nil``.
   * - ``ldap['host']``
     - |ldap host| Be sure the |chef server oec| is able to resolve any host names. Default value: ``nil``.
   * - ``ldap['login_attribute']``
     - |ldap login_attribute| For |windows ad|, this is typically ``sAMAccountName``. For |open ldap|, this is typically ``uid``. Default value: ``sAMAccountName``.
   * - ``ldap['port']``
     - |ldap port| The default value is an appropriate value for most configurations. Default value: ``389``.
   * - ``ldap['ssl_enabled']``
     - |ldap ssl_enabled| Be sure |ssl| is enabled on the |ldap| server and that the ``ldap['port']`` setting is updated with the correct value (often ``636``). Default value: ``false``.
   * - ``ldap['system_adjective']``
     - |ldap system_adjective| If a value like "corporate" is used, then the |chef server oec| user interface will display strings like "the corporate login server", "corporate login", or "corporate password." Default value: ``AD/LDAP``.

