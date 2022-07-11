PyPI Release Checklist
======================

For Every Release
-------------------

#. Update HISTORY.rst

#. Commit the changes:

    .. code-block:: bash

        git add HISTORY.rst
        git commit -m "Changelog for upcoming release 0.1.1."

#. Update version number (can also be patch or major)

    .. code-block:: bash

        bump2version minor

#. Build the package

    .. code-block:: bash

        make build

#. Run the tests:

    .. code-block:: bash

        tox

#. Push the commit:

    .. code-block:: bash

        git push

#. Push the tags, creating the new release on GitHub:

    .. code-block:: bash

        git push --tags

#. Push the package to PyPi:

    .. code-block:: bash

        python3 -m twine upload dist/*

#. Check the PyPI listing page to make sure that the README, release notes, and roadmap display properly. If not, try one of these:

    Run ``rstcheck`` to check the formatting

#. Edit the release on GitHub (e.g. https://github.com/signed-log/cookiecutter/releases). Paste the release notes into the release's release page, and come up with a title for the release.

About This Checklist
--------------------

This checklist is adapted from:

* https://gist.github.com/audreyr/5990987
* https://gist.github.com/audreyr/9f1564ea049c14f682f4

It assumes that you are using all features of Cookiecutter PyPackage.
