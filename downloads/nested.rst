Create a Nested Docs Directory
==============================

Your documentation should always be located with your source code. This allows your customers to easily find your documentation when searching the monorepo. In most cases, you create a single docset in the same directory as your code. However, if the project you are documenting does not neatly correspond to a single code directory, you should create a nested docs directory instead. 

Create a nested docs directory if the project you are documenting has one of the following qualities:

* Owned by multiple teams
* Spans multiple tools or code directories
* Does not have corresponding code
* Requires multiple product docsets

For an example of documentation that uses a nested docs directory, see the `Database documentation <http://example>`_ source code.

.. warning::
	
	Do not add documentation to generic doc directories. For example, ``~/workspace/docs/``. It is harder for your customers to find relevant documentation when it is located in these directories.

To create a nested docs directory:

#. On the command line, navigate to the ``docs/`` directory that is most relevant to your project::
	
	cd <path_to_directory>/docs/
#. Create a nested docs directory and then navigate to it::
	
	mkdir <docs_project_name> && cd <docs_project_name>
  
   Where ``<docs_project_name>`` is name of your project. 
#. Initialize your documentation project by following the procedure in `Set up Docs Project <http://example.com>`_.
#. Move the generated template files in ``docs/`` up one level and then delete the folder::

	mv docs/* . && rm -rf docs/
#. Open ``CONFIG.ini`` in a text editor and add the following line in the ``[docs]`` stanza::

	docs_dir = .

After completing the above procedure, your project has a directory structure similar to the following diagram:

.. mermaid::
   :alt: A flowchart that illustrates a nested docs directory structure. Within the project_name directory there is a docs directory. In the docs directory, there is a docs_project_name directory. In the docs_project_name directory, there are CONFIG.ini, index.rst, and template files. 

	flowchart TD
	    A(project_name) ---  B(docs)
	    B --- C(docs_project_name)
	    C --- D[CONFIG.ini]
	    C --- E[index.rst]
	    C --- F[template files]
	