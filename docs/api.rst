:mod:`zope.annotation` API
==========================


Framework Interfaces
--------------------

These interfaces define the source and targets for adaptation under the
:mod:`zope.annotation` framework:

.. automodule:: zope.annotation.interfaces

   .. autointerface::  IAnnotatable

   .. autointerface::  IAnnotations


Attribute-Based Annotations
---------------------------

The default adapter implementation uses a special attribute,
``__annotations__``, on the annotated object:

.. autoclass:: zope.annotation.attribute.AttributeAnnotations

Because setting an attribute is somewhat intrusive (as opposed to storing
annotations elsewhere), this adapter requires that its context implment
``IAttributeAnnotatable`` to signal that this attribute can be used.

.. autointerface::  zope.annotation.interfaces.IAttributeAnnotatable
