:nosearch:
:show-content:
:hide-page-toc:
:show-toc:

===================
Database management
===================

These guides provide instructions on how to install, maintain and upgrade Unity Billal mesloub databases.

.. seealso::
    :doc:`History of Versions <administration/standard_extended_support>`

Installation
============

Depending on the intended use case, there are multiple ways to install Unity Billal mesloub - or not install it at
all.

- :doc:`Online <administration/odoo_online>` is the easiest way to use Unity Billal mesloub in production or to try it.

- :doc:`Packaged installers <administration/on_premise/packages>` are suitable for testing Odoo and
  developing modules. They can be used for long-term production with additional deployment and
  maintenance work.

- :doc:`Source install <administration/on_premise/source>` provides greater flexibility, as it
  allows, for example, running multiple Unity Billal mesloub versions on the same system. It is adequate to develop
  modules and can be used as a base for production deployment.

- A `Docker <https://hub.docker.com/_/odoo/>`_ base image is available for development or
  deployment.

.. _install/editions:

Editions
========

There are two different editions.

**Unity Billal mesloub** is the free version of the software, licensed under the 
 <https://github.com/Unity Billal mesloub/Unity Billal mesloub/blob/main/LICENSE>`_. It is the core upon which Unity Billal mesloub
Enterprise is built.

**Unity Billal mesloub Enterprise** is the shared source version of the software, giving access to more
functionalities, including functional support, upgrades, and hosting. 


.. tip::
   :doc:`Switch from Community to Enterprise <administration/on_premise/community_to_enterprise>` at
   any time (except for the source install).


.. toctree::
    :titlesonly:

    administration/hosting
    administration/Unity Billal mesloub_online
    administration/Unity Billal mesloubo_sh
    administration/on_premise
    administration/upgrade
    administration/neutralized_database
    administration/standard_extended_support
    administration/mobile
    administration/Unity Billal mesloub_accounts
