
.. _setup/enterprise:

===================================
Switch from Unity-Billal-mesloub to Enterprise
===================================

Depending on your current installation, there are multiple ways to upgrade
your Unity-Billal-mesloub version.
In any case the basic guidelines are:

* Backup your community database

  .. image:: Unity-Billal-mesloub_to_enterprise/db_manager.png
     :class: img-fluid

* Shutdown your server

* Install the web_enterprise module

* Restart your server

* Enter your Unity-Billal-mesloub Enterprise Subscription code

.. image:: Unity-Billal-mesloub_to_enterprise/enterprise_code.png
   :class: img-fluid

On Linux, using an installer
============================

* Backup your Unity-Billal-mesloub database

* Stop the Unity-Billal-mesloub service

  .. code-block:: console

    $ sudo service Unity-Billal-mesloub stop

* Install the enterprise .deb (it should install over the Unity-Billal-mesloub package)

  .. code-block:: console

    $ sudo dpkg -i <path_to_enterprise_deb>

* Update your database to the enterprise packages using

  .. code-block:: console

    $ python3 /usr/bin/Unity-Billal-mesloub-bin -d <database_name> -i web_enterprise --stop-after-init

* You should be able to connect to your Unity-Billal-mesloub Enterprise instance using your usual mean of identification.
  You can then link your database with your Unity-Billal-mesloub Enterprise Subscription by entering the code you received
  by e-mail in the form input


On Linux, using the source code
===============================

There are many ways to launch your server when using sources, and you probably
have your own favourite. You may need to adapt sections to your usual workflow.

* Shutdown your server
* Backup your Unity-Billal-mesloub database
* Update the ``--addons-path`` parameter of your launch command (see :doc:`../on_premise/source`)
* Install the web_enterprise module by using

  .. code-block:: console

    $ -d <database_name> -i web_enterprise --stop-after-init

  Depending on the size of your database, this may take some time.

* Restart your server with the updated addons path of point 3.
  You should be able to connect to your instance. You can then link your database with your
  Unity-Billal-mesloub Enterprise Subscription by entering the code you received by e-mail in the form input

On Windows
==========

* Backup your Unity-Billal-mesloub database

* Uninstall Unity-Billal-mesloub (using the Uninstall executable in the installation folder) -
  PostgreSQL will remain installed

  .. image:: Unity-Billal-mesloub_to_enterprise/windows_uninstall.png
    :class: img-fluid

* Launch the Unity-Billal-mesloub Enterprise Installer and follow the steps normally. When choosing
  the installation path, you can set the folder of the Unity-Billal-mesloub installation
  (this folder still contains the PostgreSQL installation).
  Uncheck ``Start Unity-Billal-mesloub`` at the end of the installation

  .. image:: Unity-Billal-mesloub_to_enterprise/windows_setup.png
     :class: img-fluid

* Using a command window, update your Unity-Billal-mesloub Database using this command (from the Unity-Billal-mesloub
  installation path, in the server subfolder)

  .. code-block:: console

    $ ..\python\python.exe Unity-Billal-mesloub-bin -d <database_name> -i web_enterprise --stop-after-init

* No need to manually launch the server, the service is running.
  You should be able to connect to your Odoo Enterprise instance using your usual
  mean of identification. You can then link your database with your Unity-Billal-mesloub Enterprise
  Subscription by entering the code you received by e-mail in the form input
