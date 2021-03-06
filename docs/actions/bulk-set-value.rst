Bulk Set Value
==============

You can use the ``Bulk\SetValueAction`` class to specify the value of a
given field for a group of database records.

.. code-block:: phpinline

  <?php
  namespace App\Controller;

  class PostsController extends AppController
  {
      public function initialize()
      {
          parent::initialize();
          $this->Crud->mapAction('publishAll', [
              'className' => 'Crud.Bulk/SetValue',
              'field' => 'status',
              'value' => 'publish'
          ]);
      }
  }

Configuration
-------------

.. include:: /_partials/actions/configuration_intro.rst
.. include:: /_partials/actions/configuration/enabled.rst
.. include:: /_partials/actions/configuration/find_method.rst

Events
------

This is a list of events emitted from actions that extend ``Bulk\BaseAction``.

Please see the :doc:`events documentation</events>` for a full list of generic
properties and how to use the event system correctly.

.. include:: /_partials/events/startup.rst
.. include:: /_partials/events/before_filter.rst
.. include:: /_partials/events/before_bulk.rst
.. include:: /_partials/events/after_bulk.rst
.. include:: /_partials/events/set_flash.rst
.. include:: /_partials/events/before_redirect.rst
