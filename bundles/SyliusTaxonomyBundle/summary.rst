Summary
=======

Configuration Reference
-----------------------

.. code-block:: yaml

    sylius_taxonomies:
        driver: ~ # The driver used for persistence layer.
        classes:
            taxonomy:
                model: Sylius\Component\Taxonomy\Model\Taxonomy
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~ # Taxonomy repository class.
                form: Sylius\Bundle\TaxonomiesBundle\Form\Type\TaxonomyType # Taxonomy form type class name.
            taxon:
                model: Sylius\Component\Taxonomy\Model\Taxon
                controller: Sylius\Bundle\ResourceBundle\Controller\ResourceController
                repository: ~ # Taxon repository class.
                form: Sylius\Bundle\TaxonomiesBundle\Form\Type\TaxonType # Taxon form type class name.
        validation_groups:
            taxonomy: [sylius] # Taxonomy validation groups.
            taxon: [sylius] # Taxon validation groups.

Tests
-----

.. code-block:: bash

    $ composer install --dev --prefer-dist
    $ bin/phpspec run -fpretty --verbose

Bug tracking
------------

This bundle uses `GitHub issues <https://github.com/Sylius/Sylius/issues>`_.
If you have found bug, please create an issue.