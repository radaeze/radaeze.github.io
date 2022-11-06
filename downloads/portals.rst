Documentation Portal Guidelines
================================

This topic describes best practices for using documentation portals. For instructions about creating documentation portals, see `Project Templates <http://example.com>`_. For a templated example of a portal, see `Documentation Portal Template <http://example.com>`_.

Overview
--------

Documentation portals provide a curated collection of links for an engineering discipline that spans multiple teams. For example, you could represent multiple products in the machine learning discipline with a documentation portal. Portals help your customers to locate relevant information and make connections between related products. 

.. caution::

	Do not replace product documentation and team Confluence spaces with documentation portals. For more information about differences between product documentation, Confluence, and documentation portals, see `About Documentation Portals <http://example.com>`_.

Recommended Content
-------------------

Portal pages direct your customers to relevant information about your engineering discipline and its associated workflows. The following is a non-exhaustive list of pages you should include in your portal:

* **Landing Page:** Lists the teams and focus areas for your engineering discipline. This page can also include links to team roadmaps and org charts. 
* **Components:** Lists the individual products that are used in your engineering discipline. Segment these products by focus area. For each product, include information about the owning team and links to the product documentation. 
* **Radar:** Describes the release phases of products in your engineering discipline. 
* **Customer Journeys:** Lists customer journeys for your engineering discipline. Customer journeys are curated workflows for completing a task using multiple products. For each customer journey, give a brief description of the journey.
* **Support:** Lists support channels for your engineering discipline. This includes Slack channels, Jira help desks, and mailing lists. 

For an example of a documentation portal, see the `Machine Learning Portal <http://example.com>`_.

Anti-Patterns
-------------

Avoid the following anti-patterns when creating a documentation portal:

* **Including detailed organizational information:** Do not include detailed information about team policies or roadmaps. Instead, add this information to a Confluence space or Google Doc and link to it in the portal. 
* **Basing your portal on an org chart:** Avoid basing your portal around org structures to ensure it stays up-to-date. Organizations can change and their structures are not relevant to your customers. Instead, base your portal around a user persona or set of tasks.
* **Listing miscellaneous items or items with a narrow scope:** Do not create long and exhaustive lists of items with a narrow scope. For example, a list of runbooks for a single team should be added to your Confluence space instead. 

Ownership Model
---------------

Creating and maintaining a documentation portal requires collaboration between multiple teams. To ensure your portal does not become stale, you should establish an ownership model for it. Use the following guidelines for your portal ownership model:

* **Add multiple portal maintainers:** In the ownership file for your portal, add 4+ maintainers. These maintainers review documentation updates in the code review process. They should ideally be engineering managers, product managers, or team leads. Ensure that you include at least one maintainer from each team that contributes to the portal.
* **Assign contributors to update the documentation:** Ensure that these contributors are comfortable using the code review process. Ideally, all contributors should take the `Intro to Technical Writing <http://example.com>`_ course.
