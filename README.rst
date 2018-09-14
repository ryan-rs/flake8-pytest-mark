==================
Flake8-pytest-mark
==================

.. image:: https://travis-ci.org/rcbops/flake8-pytest-mark.svg?branch=master
    :target: https://travis-ci.org/rcbops/flake8-pytest-mark

Check and enforce the presence of a mark on a pytest test definition classes, methods and functions.

Quick Start Guide
-----------------

1. Install ``flake8-pytest-mark`` from PyPI with pip::

    $ pip install flake8-pytest-mark

2. Configure a mark that you would like to validate::

    $ cd project_root/
    $ vi .flake8

.. code-block:: ini

    [flake8]
    pytest_mark1 = name=test_id
                   value_match=uuid

3. Run flake8::

    $ flake8 tests/

Gotchas
-------

1. It is highly recommended to use this plugin inside of a virtualenv.
2. A configuration is required by this plugin, if none is found the plugin will throw a M401 validation error for every file.
3. By default this plug-in will enforce marks against pytest test classes. (See configuration_ for more details on how to exclude different pytest test definitions from mark checking.)

Violation Codes
---------------

All possible violation codes are documented in violation_codes_


Example Configurations
----------------------

More example configurations can be found in configuration_

Contributing
------------

See `CONTRIBUTING.rst`_  and `developer_docs.rst`_ for more details on developing for the Zigzag project.

Release Process
---------------

See `release_process.rst`_ for information on the release process for 'zigzag'

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _CONTRIBUTING.rst: CONTRIBUTING.rst
.. _developer_docs.rst: docs/developer_docs.rst
.. _release_process.rst: docs/release_process.rst
.. _configuration: docs/configuration.rst
.. _violation_codes: docs/violation_codes.rst
.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
