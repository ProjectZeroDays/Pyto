Using Django
============

Django works in Pyto but with some limitations. To use Django, first install it. Go to the PyPi section and search for Django.
Once it's installed, you can create a project (if you don't already have one). Go to the "Run module" section. Then press the folder icon at the top right and select the folder where your project will be located. After that run ``django-admin startproject <project_name>``. A project will be created in the previously selected folder.

You can now open the ``manage.py`` file inside the project. Press the Settings icon, then "Arguments" and type this: ``runserver --noreload --nothreading``.
Edit the script and replace this:

.. highlight:: python
.. code-block:: python

    if __name__ == '__main__':
        main()
        
by this:

.. highlight:: python
.. code-block:: python

    if __name__ == '__main__':
        import background as bg
        with bg.BackgroundTask() as b:
            main()

You can now run your server by running ``manage.py``.

.. raw:: html

    <video width="100%" controls>
      <source src="https://pyto.app/assets/django.mp4" type="video/mp4">
    </video>
