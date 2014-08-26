Summary
=======

Configuration Reference
-----------------------

.. code-block:: yaml

    sylius_taxation:
        driver: ~ # The driver used for persistence layer.
        classes:
            tax_category:
                model: Sylius\Component\Taxation\Model\TaxCategory
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~
                form: Sylius\Bundle\TaxationBundle\Form\Type\TaxCategoryType
            tax_rate:
                model: Sylius\Component\Taxation\Model\TaxRate
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~
                form: Sylius\Bundle\TaxationBundle\Form\Type\TaxRateType
        validation_groups:
            tax_category: [sylius]
            tax_rate: [sylius]

Tests
-----

.. code-block:: bash

    $ composer install --dev --prefer-dist
    $ bin/phpspec run -fpretty --verbose

Bug tracking
------------

This bundle uses `GitHub issues <https://github.com/Sylius/Sylius/issues>`_.
If you have found bug, please create an issue.