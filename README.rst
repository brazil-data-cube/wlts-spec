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

.. image:: https://img.shields.io/badge/lifecycle-maturing-blue.svg
        :target: https://www.tidyverse.org/lifecycle/#maturing
        :alt: Software Life Cycle

.. image:: https://img.shields.io/github/tag/brazil-data-cube/wlts-spec.svg
        :target: https://github.com/brazil-data-cube/wlts-spec/releases
        :alt: Release

.. image:: https://img.shields.io/discord/689541907621085198?logo=discord&logoColor=ffffff&color=7389D8
        :target: https://discord.com/channels/689541907621085198#
        :alt: Join us at Discord

About
=====

Land Use and Cover information is essential to support governments in decision making on the impact of human activities on the environment, for planning the use of natural resources, conservation of biodiversity, and monitoring climate change.


Currently, several projects systematically provide information on the dynamics of land use and cover. Well known projects include PRODES, DETER and TerraClass. These projects are developed by INPE and they produce information on land use and coverage used by the Brazilian Government to make public policy decisions. Besides these projects there are other initiatives from universities and space agencies devoted to the creation of national and global maps.


Although these projects adhere to open data policies and provide a rich collection of data, there still a gap in the integrated use of these collections: it requires from researchers, students and public officials a great effort to collect, organize and integrate all the datasets, prior to their use. In general, each collection adopts its own land use and cover classification system, with class names and meanings very different across the collections. Besides that, the collections have diffrent spatial and temporalresolutions, relies on different data representation (raster or vector) and served by diffrent systems or formats (files, database or web services).


In this context, the **W**\ eb **L**\ and **T**\ rajectory **S**\ ervice (WLTS) is a service that aims to facilitate the access to these various "land use and cover" data collections through a tailored API. The result is tool that allows researchers and specialists to spend their time in the analytical process, once the API provides the integration of these datasets and brings the concept of Land Use and Cover Trajectories as a high level abstraction. The WLTS approach is to use a data model that defines a minimum set of temporal and spatial information to represent different sources and types of data. WLTS can be used in a range of application, such as in validation of land cover data sets, in the selection of trainning samples to support Machine Learning algorithms used in the generation of new classification maps.


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
    Copyright (C) 2019-2020 INPE.

    Web Land Trajectory Service is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.
