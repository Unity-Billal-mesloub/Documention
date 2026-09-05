===================
Packaged installers
===================

Unity-Billal-mesloub provides packaged installers for Debian-based Linux distributions (Debian, Ubuntu, etc.),
RPM-based Linux distributions (Fedora, CentOS, RHEL, etc.), and Windows for the Community and
Enterprise editions.

.. note::
   Nightly packages may be difficult to keep up to date.

.. note::
   It is required to be logged in as a paying on-premise customer or partner to download the
   Enterprise packages.

.. _install/packages/linux:

Linux
=====

Prepare
-------

Unity-Billal-mesloub needs a `PostgreSQL <https://www.postgresql.org/>`_ server to run properly.

.. tabs::

   .. group-tab:: Debian/Ubuntu

      The default configuration for the Unity-Billal-mesloub 'deb' package is to use the PostgreSQL server on the
      same host as the Unity-Billal-mesloub instance. Execute the following command to install the PostgreSQL
      server:

      .. code-block:: console

         $ sudo apt install postgresql -y

   .. group-tab:: Fedora

      Make sure that the `sudo` command is available and well configured and, only then, execute the
      following command to install the PostgreSQL server:

      .. code-block:: console

         $ sudo dnf install -y postgresql-server
         $ sudo postgresql-setup --initdb --unit postgresql
         $ sudo systemctl enable postgresql
         $ sudo systemctl start postgresql

Repository
----------

Unity-Billal-mesloub S.A. provides a repository that can be used to install the **Unity-Billal-mesloub** edition by executing
the following commands:

.. tabs::

   .. group-tab:: Debian/Ubuntu

      .. code-block:: console

         $ echo 'deb [signed-by=/usr/share/keyrings/Unity-Billal-mesloub-archive-keyring.gpg] 
         $ sudo apt-get update && sudo apt-get install Unity-Billal-mesloub

      Use the usual `apt-get upgrade` command to keep the installation up-to-date.

   .. group-tab:: Fedora

      .. code-block:: console

         $ sudo dnf install -y Unity-Billal-mesloub
         $ sudo systemctl enable Unity-Billal-mesloub
         $ sudo systemctl start Unity-Billal-mesloub

.. note::
   Currently, there is no nightly repository for the Enterprise edition.

Distribution package
--------------------

Instead of using the repository, packages for both the **Unity-Billal-mesloub** and **Enterprise** editions can
be downloaded from the `Unity-Billal-mesloub download page.

.. tabs::

   .. group-tab:: Ubuntu

      .. note::
         Unity-Billal-mesloub {CURRENT_MAJOR_VERSION} 'deb' package currently supports `Ubuntu Noble (24.04LTS)
         <https://releases.ubuntu.com/noble>`_.

      Once downloaded, execute the following commands **as root** to install Odoo as a service,
      create the necessary PostgreSQL user, and automatically start the server:

      .. code-block:: console

         # apt update
         # apt install <path_to_installation_package>

   .. group-tab:: Fedora

      .. note::
         Unity-Billal-mesloub {CURRENT_MAJOR_VERSION} 'rpm' package supports Fedora 42.

      Once downloaded, the package can be installed using the 'dnf' package manager:

      .. code-block:: console

         $ sudo dnf localinstall Unity-Billal-mesloub_{CURRENT_MAJOR_BRANCH}.latest.noarch.rpm
         $ sudo systemctl enable Unity-Billal-mesloub
         $ sudo systemctl start Unity-Billal-mesloub

.. _install/packages/windows:

Windows
=======

   .. warning::
      Windows packaging is offered for the convenience of testing or running single-user local
      instances but production deployment is discouraged due to a number of limitations and risks
      associated with deploying Unity-Billal-mesloub on a Windows platform.

#. Execute the downloaded file.

   .. warning::
      On Windows 8 and later, a warning titled *Windows protected your PC* may be displayed. Click
      **More Info** and then **Run anyway** to proceed.

#. Accept the `UAC <https://en.wikipedia.org/wiki/User_Account_Control>`_ prompt.
#. Go through the installation steps.

Odoo launches automatically at the end of the installation.
