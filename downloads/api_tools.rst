API Documentation Tools
=======================

This page describes tools for auto-generating API documentation.

Generating Python and REST API documentation is natively supported by our internal documentation tooling. Because our internal documentation tooling provides limited support for other languages, engineering teams have developed custom tools for generating other types of API documentation. 

The following table lists tools for auto-generating API documentation:

.. list-table::
    :widths: 10 55 10 10 10 
    :header-rows: 1

    * - Tool
      - Description 
      - API Type
      - Native Support
      - Documentation 
    * - **Python sub-command**
      - Generates documentation for Python modules, classes, and functions. Use this sub-command to do the following:

      	- Automatically update API documentation with source code changes
      	- Manually generate API documentation 
      - Python
      - ✅
      - `Generate API Documentation <https://example.com>`_ 
    * - **Sphinx Autodoc extension**
      - Includes Python code from source code doctrings. Use this extension to generate API documentation inline with content you write.
      - Python
      - ✅
      - `Include API Documentation Inline <https://example.com>`_     
    * - **Sphinx Httpdomain directive**
      - Embeds REST API documentation inline with content you write. 
      - REST
      - ✅
      - `Document REST APIs <https://example.com>`_
    * - **Bazel**
      - Generates Scaladocs for a Scala library target. For an example of documentation that uses this tool, see the `Scala API documentation <https://example.com>`_. 
      - Scala
      - ❌
      - `Build Scaladocs Documentation <https://example.com>`_
    * - **DocC**
      - Creates DocC documentation from source comments. For an example of documentation that uses this tool, see the `Mobile API Documentation <https://example.com>`_.
      - Swift
      - ❌
      - `Build DocC Documentation <https://example.com>`_