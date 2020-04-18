..
    This file is part of Web Land Trajectory Service Specification.
    Copyright (C) 2019 INPE.

   Web Land Trajectory Service Specification is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.


==================================
Web Land Trajectory Service - Spec
==================================


.. image:: https://img.shields.io/badge/license-MIT-green
        :target: https://github.com//brazil-data-cube/wlts-spec/blob/master/LICENSE
        :alt: Software License

.. image:: https://img.shields.io/badge/lifecycle-experimental-orange.svg
        :target: https://www.tidyverse.org/lifecycle/#experimental
        :alt: Software Life Cycle

.. image:: https://img.shields.io/github/tag/brazil-data-cube/wlts-spec.svg
        :target: https://github.com/brazil-data-cube/wlts-spec/releases
        :alt: Release

.. image:: https://badges.gitter.im/brazil-data-cube/community.svg/
        :target: https://gitter.im/brazil-data-cube/community#
        :alt: Join the chat

About
=====

Land Use and Cover informations is essential to support governments in decision making on the impact of human activities on the environment, for planning the use of natural resources, conservation of biodiversity, monitoring climate change.

Currently, several projects systematically provide information on the dynamics of land use and cover. PRODES, DETER and TerraClass are projects developed by INPE, which produce information on land use and coverage used by the Brazilian government to make public policy decisions. PRODES, DETER and TerraClass have as methodology the visual interpretation of the data obtained by Earth observation satellites. Other projects use machine learning methods to process spatial data, such as MapBiomas. On a global scale, Global Land Cover 2000 (GLC-2000) uses different classification techniques, based on the requirements and preferences of partner institutions around the world.

Although these projects provide, in an open manner, a rich collection of data, the integrated use of these collections require a major effort to collect, organize and integration, prior to their use by scientists, students and public officials. Each collection has different classification systems, temporal and spatial resolution, storage structure (raster or vector).

In this context, the **W**\ eb **L**\ and **T**\ rajectory **S**\ ervice or, for short, **WLTS**, is a service that aims to facilitate access to these various collections through an API designed to integrate spatial data from different types of data sources, abstract queries to databases available data, allowing researchers and specialists to improve their analysis, integrating these trajectories with time series extracted from remote sensing images, validating new land cover data sets and selecting training samples to use in the generation of new classification maps. The WLTS approach is to use a data model that defines a minimum set of temporal and spatial information to represent different sources and types of data.

Free and Open Source implementations based on this service can be found in the `wlts <https://github.com/brazil-data-cube/wlts>`_ (server) and `wlts.py <https://github.com/brazil-data-cube/wlts.py>`_ (Python client). See also the service **LCCS-WS** (**L**\ and **C**\ over **C**\ lassification **S**\ystem **W**\eb **S**\ ervice) (`LCCS-WS <https://github.com/brazil-data-cube/lccs-ws-spec>`_) which is used to represent the classes associated with the resources retrieved in the queries.


Repository Organization
=======================

- `api <./api>`_: WLTS Specification using `OpenAPI 3.0 <https://github.com/OAI/OpenAPI-Specification>`_.

- `jsonschemas <./jsonschemas>`_: `JSON Schema <https://json-schema.org/>`_ for the classification systems and classes.

Building the Documentation
==========================

Requirements
------------

The build system for the REST API documentation relies on the Node.js run-time environment:

  - `Node.js <https://nodejs.org/en/>`_ (Version 8+).

  - `ReDoc <https://github.com/Redocly/redoc>`_: generates HTML reference documentation from an OpenAPI specification file.


Build
-----

If you have Node.js installed, please, execute the following command to install the ReDoc dependency:

.. code-block:: shell

    $ npm install


After that, generate the documentation:

.. code-block:: shell

    $ npm run build


The above command will create a folder named ``dist`` with the bundled file index.html. You may open it in your web browser or may serve it with an HTTP Server.

For Python developers, you can serve the HTML with:

.. code-block:: shell

        python3.7 -m http.server 8080 --directory dist


License
=======

.. admonition::
    Copyright (C) 2019 INPE.

    Web Land Trajectory Service is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.