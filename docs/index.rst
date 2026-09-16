``saltext-openrc``: Salt Extension for OpenRC
==============================================

This extension provides an execution module for managing services on systems
that use `OpenRC <https://github.com/OpenRC/openrc>`_ as their init system.

- **service** (``saltext.openrc.modules.openrc``) -- service management via
  ``rc-service``, ``rc-update`` and ``rc-status``

The module registers under Salt's standard ``service`` virtual name, so
existing states such as ``service.running`` and ``service.dead`` work on
managed minions without any changes to your state files.

The module loads on any system where the ``rc-service`` command is present,
so it works across OpenRC-based distributions (Alpine, Gentoo, Artix, Devuan
with OpenRC, and so on) rather than being tied to a single OS family. See the
``__virtual__`` docstring in ``src/saltext/openrc/modules/openrc.py`` if you
need a stricter check that only loads when OpenRC is actually in use (rather
than merely installed).

.. toctree::
  :maxdepth: 2
  :caption: Guides
  :hidden:

  topics/installation

.. toctree::
  :maxdepth: 2
  :caption: Provided Modules
  :hidden:

  ref/modules/index

.. toctree::
  :maxdepth: 2
  :caption: Reference
  :hidden:

  changelog


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
