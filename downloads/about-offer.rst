About Service Offerings
=======================

This topic describes the structure of a Tanzu Service Manager (TSMGR) service offering and how an offering displays on ``cf marketplace``.

Overview
--------

A ``cf marketplace`` service offering includes the following:

+ **One or more Helm charts:** You must configure a Helm chart to be compatible with TSMGR. For more information, see `Configuring a Helm Chart <https://www.example.com>`_.
+ **A TSMGR package:** This package contains YAML files that TSMGR uses to customize your service offering. For more information, see `Preparing a Service Offering <http://www.example.com>`_.

Service Offering Directory Structure
------------------------------------

The following code snippet shows an example of a service offering directory structure:

.. code-block:: yaml

    service-name/
       bind.yaml
       ksm.yaml
       plans.yaml
       overrides/
         override-values.yaml
       plans/
         small.yaml
         medium.yaml
       resource-quotas/
         quota.yaml

    helm-chart.tgz


In the above example:

+  ``service-name/`` is the directory for the TSMGR package. Depending on your customization, you must include some or all of the above YAML files and subdirectories in the TSMGR package.

+ ``helm-chart.tgz`` is the Helm chart for the service offering.

To determine which files you must include in your TSMGR package, reference the following table:

.. flat-table::
  :header-rows: 1
  :widths: 20 10 20

  * - Task
    - Required File
    - Documentation
  * - Suppress services credentials output when a developer binds a service instance
    - ``bind.yaml``
    - `(Optional) Create Binding Template for App Consumption <https://www.example.com>`_
  * - Add a custom ``cf marketplace`` name
    - :rspan:`3` ``ksm.yaml``
    - `Service Offerings in CF Marketplace <https://www.example.com>`_
  * - Offer more than one Helm chart
    - `(Optional) Offer Multiple Charts in a Single Offering <https://example.com>`_
  * - Add a service offering with an Operator pattern
    - `Operators <https://kubernetes.io/docs/concepts/extend-kubernetes/operator>`_
  * - Override default chart values
    - `(Optional) Override Chart Values <https://www.example.com>`_
  * - Create a non-default plan in ``cf marketplace``
    - :rspan:`2` ``plans.yaml``
    - :rspan:`2` `(Optional) Define Plans Configuration <https://www.example.com>`_
  * - Provision a service on a non-default cluster
  * - Define resource quotas that limit memory and CPU consumption
 

Service Offerings in CF Marketplace
-----------------------------------

If you upload a Helm chart with either a ``ksm.yaml`` or ``plans.yaml`` file, TSMGR
overrides the default values for the service offering name, description, and plan names.
These values are displayed when a Tanzu developer runs ``cf marketplace``.

The following table describes the values that TSMGR uses when you upload a Helm chart either without additional configurations, with a ``ksm.yaml`` file, or with a ``plans.yaml`` file:

.. flat-table::
  :header-rows: 1
  :widths: 5 15 15 15

  * - Additional Configuration File
    - Name
    - Description
    - Plan
  * - **None**
    - ``name`` value in ``Chart.yaml``
    - ``description`` value in ``Chart.yaml``
    - ``default``
  * - ``ksm.yaml``
    - ``marketplace-name`` value in ``ksm.yaml`` 
    - Default value
    - Default value
  * - ``plans.yaml``
    - Default value
    - For each plan, ``description`` value in ``plans.yaml``
    - For each plan, ``name`` value in ``plans.yaml``