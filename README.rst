..
    This file is part of Web Land Trajectory Service Specification.
    Copyright (C) 2019 INPE.

   Web Land Trajectory Service Specification is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.


==================================
Web Land Trajectory Service - Spec
==================================



Structure
=========

- api_- Represents WLTS API Versions specification containing URL signatures
- json-schemas_


.. _Api: ./api
.. _json-schemas: ./json-schemas

Build Documentation
===================

Requirements

- Node_:(NodeJS 8+)
- ReDoc_

.. _Node: https://nodejs.org/en/
.. _ReDoc: https://github.com/Redocly/redoc


Execute the following command to install *node modules* dependencies:

.. code-block:: shell

        npm install

After that, generate WLTS documentation:

.. code-block:: shell

        npm run build

It will create folder *dist* with a bundled file *index.html*. You may serve this file with HTTP Server.