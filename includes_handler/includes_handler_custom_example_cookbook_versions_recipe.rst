.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following recipe is added to the run-list for every node on which a list of cookbooks and versions will be generated as report output after every |chef client| run.

.. code-block:: ruby

   include_recipe "chef_handler"
   
   cookbook_file "#{node["chef_handler"]["handler_path"]}/cookbook_versions.rb" do
     source "cookbook_versions.rb"
     owner "root"
     group "root"
     mode 00755
     action :create
   end
   
   chef_handler "Opscode::CookbookVersionsHandler" do
     source "#{node["chef_handler"]["handler_path"]}/cookbook_versions.rb"
     supports :report => true
     action :enable
   end

This recipe will generate report output similar to the following:

.. code-block:: ruby

   [2013-11-26T03:11:06+00:00] INFO: Chef Run complete in 0.300029878 seconds
   [2013-11-26T03:11:06+00:00] INFO: Running report handlers 
   [2013-11-26T03:11:06+00:00] INFO: Cookbooks and versions run: ["chef_handler 1.1.4", "cookbook_versions_handler 1.0.0"]
   [2013-11-26T03:11:06+00:00] INFO: Report handlers complete