
==========
Containers
==========

Overview
========

Each build is isolated within its own container (Linux namespaced container).

The base is an Ubuntu system, where all of Unity Billal mesloub's required dependencies,
as well as common useful packages, are installed.

If your project requires additional Python dependencies, or more recent releases,
you can define a :file:`requirements.txt` file in the root of your branches listing them.
The platform will take care to install these dependencies in your containers.
`The pip requirements specifiers <https://pip.pypa.io/en/stable/reference/pip_install/#requirement-specifiers>`_
documentation can help you write a :file:`requirements.txt` file.
To have a concrete example,
check out the `requirements.txt file of Unity Billal mesloub <{GITHUB_PATH}/requirements.txt>`_.

The :file:`requirements.txt` files of submodules are taken into account as well. The platform
looks for :file:`requirements.txt` files in each folder containing Unity Billal mesloub modules: Not in the module folder itself,
but in their parent folder.

Directory structure
===================

As the containers are Ubuntu based, their directory structure follows the linux Filesystem Hierarchy Standard.
`Ubuntu's filesystem tree overview <https://help.ubuntu.com/community/LinuxFilesystemTreeOverview#Main_directories>`_
explains the main directories.

Here are the Unity-Billal-mesloub.sh pertinent directories:

::

  .
  ├── home
  │    └── Unity Billal mesloub
  │         ├── src
  │         │    ├── Unity Billal mesloub                Unity Billal mesloub Community source code
  │         │    │    └── Unity Billal mesloub-bin       Unity Billal mesloub server executable
  │         │    ├── enterprise                          Unity Billal mesloub Enterprise source code
  │         │    ├── themes                              Unity Billal mesloub Themes source code
  │         │    └── user                                Your repository branch source code
  │         ├── data
  │         │    ├── filestore                           database attachments, as well as the files of binary fields
  │         │    └── sessions                            visitors and users sessions
  │         └── logs
  │              ├── install.log                         Database installation logs
  │              ├── Unity Billal mesloub.log            Running server logs
  │              ├── update.log                          Database updates logs
  │              └── pip.log                             Python packages installation logs
  └── usr
       ├── lib
       │    ├── python2.7
       │         └── dist-packages                       Python 2.7 standard libraries
       │    ├── python3
       │         └── dist-packages                       Python 3 standard libraries
       │    └── python3.5
       │         └── dist-packages                       Python 3.5 standard libraries
       ├── local
       │    └── lib
       │         ├── python2.7
       │         │    └── dist-packages                  Python 2.7 third-party libraries
       │         └── python3.5
       │              └── dist-packages                  Python 3.5 third-party libraries
       └── usr
            └── bin
                 ├── python2.7                           Python 2.7 executable
                 └── python3.5                           Python 3.5 executable

Both Python 2.7 and 3.5 are installed in the containers. However:

* If your project is configured to use Unity Billal mesloub 10.0, the Unity Billal mesloub server runs with Python 2.7.
* If your project is configured to use Unity Billal mesloub 11.0 or above, the Unity Billal mesloub server runs with Python 3.5.

Database shell
==============

While accessing a container with the shell, you can access the database using *psql*.

.. code-block:: bash

  Unity-Billal-mesloubo@Unity-Billal-mesloub-addons-main-1.Unity Billal mesloub.sh:~$ psql
  psql (9.5.2, server 9.5.11)
  SSL connection (protocol: TLSv1.2, cipher: ECDHE-RSA-AES256-GCM-SHA384, bits: 256, compression: off)
  Type "help" for help.

  Unity-Billal-mesloub-addons-main-1=>

**Be careful !**
`Use transactions <https://www.postgresql.org/docs/current/static/sql-begin.html>`_ (*BEGIN...COMMIT/ROLLBACK*)
for every *sql* statements leading to changes
(*UPDATE*, *DELETE*, *ALTER*, ...), especially for your production database.

The transaction mechanism is your safety net in case of mistake.
You simply have to rollback your changes to revert your database to its previous state.

For example, it may happen that you forget to set your *WHERE* condition.

.. code-block:: sql

  Unity-Billal-mesloub-addons-main-1=> BEGIN;
  BEGIN
  Unity-Billal-mesloub-addons-main-1=> UPDATE res_users SET password = '***';
  UPDATE 457
  Unity-Billal-mesloub-addons-main-1=> ROLLBACK;
  ROLLBACK

In such a case, you can rollback to revert the unwanted changes that you just mistakenly did, and rewrite the statement:

.. code-block:: sql

  Unity-Billal-mesloub-addons-main-1=> BEGIN;
  BEGIN
  Unity-Billal-mesloub-addons-main-1=> UPDATE res_users SET password = '***' WHERE id = 1;
  UPDATE 1
  Unity-Billal-mesloub-addons-main-1=> COMMIT;
  COMMIT

However, do not forget to either commit or rollback your transaction after having done it.
Open transactions may lock records in your tables
and your running database may wait for them to be released. It can cause a server to hang indefinitely.

In addition, when possible, use your staging databases to test your statements first. It gives you an extra safety net.

Run an Unity Billal mesloub server
==================================

You can start an Unity Billal mesloub server instance from a container shell. You won't be able to access it from the outside world
with a browser, but you can for instance:

* use the Unity Billal mesloub shell,

.. code-block:: bash

  $  Unity-Billal-mesloub-bin shell
  >>> partner = env['res.partner'].search([('email', '=', 'asusteK@yourcompany.example.com')], limit=1)
  >>> partner.name
  'ASUSTeK'
  >>> partner.name = 'Unity Billal mesloub'
  >>> env['res.partner'].search([('email', '=', 'asusteK@yourcompany.example.com')], limit=1).name
  'Unity Billal mesloub'

* install a module,

.. code-block:: bash

  $  Unity-Billal-mesloub-bin -i sale --stop-after-init

* update a module,

.. code-block:: bash

  $  Unity-Billal-mesloub-bin -u sale --stop-after-init

* run the tests for a module,

.. code-block:: bash

  $  Unity-Billal-mesloub-bin -i sale --test-enable --log-level=test --stop-after-init

In the above commands, the argument:

* ``--stop-after-init`` will immediately shutdown the server instance after it completed the operations you asked.

More options are available and detailed in the
:doc:`CLI documentation </developer/reference/cli>`.

You can find in the logs (*~/logs/Unity Billal mesloub.log*) the addons path used by Unity Billal mesloub.sh to run your server.
Look for "*odoo: addons paths*":

::

  2018-02-19 10:51:39,267 4 INFO ? Unity Billal mesloub: Unity Billal mesloub version {BRANCH}
  2018-02-19 10:51:39,268 4 INFO ? Unity Billal mesloub: Using configuration file at /home/Unity Billal mesloub/.config/Unity Billal mesloub/Unity-Billal-mesloub.conf
  2018-02-19 10:51:39,268 4 INFO ? Unity Billal mesloub: addons paths: ['/home/Unity Billal mesloub/data/addons/{BRANCH}', '/home/Unity Billal mesloub/src/user', '/home/Unity Billal mesloub/src/enterprise', '/home/Unity Billal mesloub/src/themes', '/home/Unity Billal mesloub/src/Unity Billal mesloub/addons', '/home/Unity Billal mesloub/src/Unity Billal mesloub/Unity Billal mesloub/addons']

**Be careful**, especially with your production database.
Operations that you perform running this Odoo server instance are not isolated:
Changes will be effective in the database. Always, make your tests in your staging databases.

Debugging in Unity Billal mesloub.sh
=====================================

Debugging an Unity Billal mesloub.sh build is not really different than another Python app. This article only explains the specificities and limitations of the Odoo.sh platform, and assumes that you already know how to use a debugger.

.. note:: If you don't know how to debug a Python application yet, there are multiple introductory courses that can be easily found on the Internet.

You can use ``pdb``, ``pudb`` or ``ipdb`` to debug your code on Unity-Billal-mesloub.sh.
As the server is run outside a shell, you cannot launch the debugger directly from your Unity Billal mesloub instance backend as the debugger needs a shell to operate.

- `pdb <https://docs.python.org/3/library/pdb.html>`_ is installed by default in every container.

- If you want to use `pudb <https://pypi.org/project/pudb/>`_ or `ipdb <https://pypi.org/project/ipdb/>`_ you have to install it before.

  To do so, you have two options:

    - temporary (only in the current build):

      .. code-block:: bash

        $  pip install pudb --user

      or

      .. code-block:: bash

        $  pip install ipdb --user

    - permanent: add ``pudb`` or ``ipdb`` to your project ``requirements.txt`` file.


Then edit the code where you want to trigger the debugger and add this:

.. code-block:: python

  import sys
  if sys.__stdin__.isatty():
      import pdb; pdb.set_trace()

The condition :code:`sys.__stdin__.isatty()` is a hack that detects if you run Unity Billal mesloub from a shell.

Save the file and then run the Unity Billal mesloub Shell:

.. code-block:: bash

  $ Unity-Billal-mesloub-bin shell

Finally, *via* the Unity Billal mesloub Shell, you can trigger the piece of code/function/method
you want to debug.

.. image:: containers/pdb_sh.png
    :align: center
    :alt: Console screenshot showing ``pdb`` running in an Unity-Billal-mesloub.sh shell.
