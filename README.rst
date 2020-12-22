==========================================================
`pickle5` -- A backport of the pickle 5 protocol (PEP 574)
==========================================================

This repo is a mirror of `pickle5-backport <https://github.com/pitrou/pickle5-backport>`_ , but with scripts that build and test python wheels.

This package backports all features and APIs added in the ``pickle`` module
in Python 3.8.3, including the
`PEP 574 <https://www.python.org/dev/peps/pep-0574/>`_ additions.  It should
work with Python 3.5, 3.6 and 3.7.

Basic usage is similar to the ``pickle`` module, except that the module
to be imported is ``pickle5``:

.. code-block:: python

   import pickle5 as pickle

   pb = pickle.PickleBuffer(b"foo")
   data = pickle.dumps(pb, protocol=5)
   assert pickle.loads(data) == b"foo"

Detailed documentation can be found in PEP 574 and the standard
`pickle documentation <https://docs.python.org/3.8/library/pickle.html>`_.

.. image:: https://github.com/suquark/pickle5-backport/workflows/Build/badge.svg
   :target: https://github.com/suquark/pickle5-backport/actions
   :align: left
