Summary
=======

Configuration reference
-----------------------

.. code-block:: yaml

    sylius_cart:
        driver: ~ # The driver used for persistence layer.
        resolver: ~ # Service id of cart item resolver.
        provider: sylius.cart_provider.default # Cart provider service id.
        storage: sylius.cart_storage.session # The id of cart storage for default provider.
        classes:
            cart:
                controller: Sylius\Bundle\CartBundle\Controller\CartController
                form: Sylius\Bundle\CartBundle\Form\Type\CartType # The form type name to use.
            item:
                controller: Sylius\Bundle\CartBundle\Controller\CartItemController
                form: Sylius\Bundle\CartBundle\Form\Type\CartItemType # The form type class name to use.
        validation_groups:
            cart: [sylius] # Cart validation groups.
            item: [sylius] # Cart item validation groups.

`phpspec2 <http://phpspec.net>`_ examples
-----------------------------------------

.. code-block:: bash

    $ composer install --dev --prefer-dist
    $ bin/phpspec run -f pretty


Bug tracking
------------

This bundle uses `GitHub issues <https://github.com/Sylius/Sylius/issues>`_.
If you have found bug, please create an issue.
