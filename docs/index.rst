os-release Documentation
========================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

.. image:: https://img.shields.io/pypi/v/os-release
    :target: https://pypi.org/project/os-release/
    :alt: os-release on PyPI

*os-release* is a simple Python module for reading systemd's ``os-release`` information on modern Linux distributions.

It parses the contents of systemd's `os-release(5)`_ files:
`/etc/os-release` or `/usr/lib/os-release`.

Installation
------------

*os-release* is available on `PyPI <https://pypi.org/project/os-release/>`_.

Add it to your projects ``setup.py` ``install_requires``::

    install_requires=['os-release']

or install it directly via ``pip``::

    $ pip install os-release

Alternatively, clone the `Git repository <https://github.com/zegelin/python-os-release>`_ and run::

    $ python setup.py install


Quick Start
-----------

The most common usage of this module is to call the :py:meth:`os_release.current_release` method to obtain the details
of the operating system on which the calling Python program is running.

For example, on a CentOS 8 system::

    >>> import os_release
    >>> os_release.current_release()
    OsRelease(
        name='CentOS Linux',
        version='8 (Core)',
        id='centos',
        id_like=('rhel', 'fedora'),
        version_codename=None,
        version_id='8',
        pretty_name='CentOS Linux 8 (Core)',
        ansi_color='0;31',
        cpe_name='cpe:/o:centos:centos:8',
        build_id=None,
        variant=None,
        variant_id=None,
        logo=None,
        urls=Urls(
            home='https://www.centos.org/',
            documentation=None,
            support=None,
            bug_report='https://bugs.centos.org/',
            privacy_policy=None
        ),
        vendor_extra={
            'PLATFORM_ID': 'platform:el8',
            'CENTOS_MANTISBT_PROJECT': 'CentOS-8',
            'CENTOS_MANTISBT_PROJECT_VERSION': '8',
            'REDHAT_SUPPORT_PRODUCT': 'centos',
            'REDHAT_SUPPORT_PRODUCT_VERSION': '8'
        }
    )



API
---

.. automodule:: os_release
   :members:
   :member-order: bysource

.. automodule:: os_release.parser

.. _os-release(5): https://www.freedesktop.org/software/systemd/man/os-release.html

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
