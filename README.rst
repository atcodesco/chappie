
A python module including common tools and utilities for python projects.


Environment variables
---------------------

- CHAPPIE_AWS_PROFILE
    if it doesn't exist, it take the default profile.
- CHAPPIE_STORAGE_SERVICE
    if it doesn't exist, set "localsystem" by default.
- CHAPPIE_STORAGE_BUCKET_NAME
    if it doesn't exist, it take create a bucket called "main-storage-bucket-nQHNUWM4u8jAkcxU" inside a folder called "file_manager".
- CHAPPIE_NOTIFIER_SERVICE
    define service to use for notify exceptions or simple message. rollbar is used by default.


Updating Distribution
---------------------

- run tests

.. code:: sh

    python -m unittest discover tests

- Modify the version number in setup.py (major.minor.bugfix)

.. code:: sh

    python setup.py sdist

Installation
------------

- Create a virtual environment
- Activate the virtual environment
- Install the chappie utilities

.. code:: sh

    virtualenv -p python3 venv

    . venv/bin/activate

    pip install -U -e git+ssh://git@github.com/atcodes-development/chappie.git@master#egg=chappie; pip freeze > requirements.txt
