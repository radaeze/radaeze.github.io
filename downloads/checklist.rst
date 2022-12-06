Platform Operator Getting Started Guide
=======================================

This topic provides an overview for configuring and installing Tanzu Service Manager (TSMGR).


Getting Started Task List
-------------------------

To get started with TSMGR:

#. **Install and configure a Kubernetes cluster:** TSMGR supports Tanzu Kubernetes Grid Integrated Edition (TKGI) clusters. For information about TKGI, see `Tanzu Kubernetes Grid Integrated Edition <https://docs.pivotal.io/tkgi/index.html>`_.

#. **Install and configure TSMGR:** You can choose to quickly install TSMGR for evaluation purposes or to install it with a configuration for a production environment.
    
   * For lab and evaluation environments, see `Installing and Configuring in Development Mode <https://www.example.com>`_.
   * For production environments, see `Installing and Configuring <https://www.example.com>`_.

#. **Configure the TSMGR CLI:** See `Configure the TSMGR CLI <https://www.example.com>`_.

#. **Register your Kubernetes workload clusters with TSMGR:** You can either register clusters individually or set a default cluster. See `Register a Kubernetes Cluster <https://www.example.com>`_ or `Set a Default Kubernetes Cluster <https://www.example.com>`_.

#. **Add an example service offering:** For evaluation or testing purposes, add the Bitnami MySQL chart to TSMGR.

   To add the Bitnami MySQL chart:

   #. Clone the ``bitnami/charts`` repo::

          git clone https://github.com/bitnami/charts.git
          
   #. Add the MySQL service offering by following the procedure in `Add a Service Offering to TSMGR <https://www.example.com>`_.

#. **Enable developer access to the service offering:** See `Enable Service Offering Access <https://www.example.com>`_.

Next Steps
----------

After completing the process outlined above,
developers can use Cloud Foundry Command Line Interface (cf CLI) commands to
manage a MySQL service instance. This service instance runs on a Kubernetes cluster.

To add additional services to your marketplace, follow the procedures in `Configuring a Helm Chart <https://www.example.com>`_ and `Preparing a Service Offering <https://www.example.com>`_. 