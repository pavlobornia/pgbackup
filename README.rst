pgbackup
=========

CLI for backup remote PostgreSQL database either locally or to S3.

Preparing for Development
-------------------------

1. Ensure ``pip`` and ``pipenv`` are installed.
2. Clone repository: ``git clone git@github.com:pavlobornia/pgbackup.git``
3. ``cd`` into the repository
4. Fetch development dependencies ``make install``
5. Activate virtualenv ``pipenv shell``

Usage
-----

Pass in a full database URL, the storage driver, and the destination.

S3 Example w/ bucket name:

::

  $ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups

Local Example w/ local path:

::

  $ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/backups

Running Tests
-------------

Run tests locally using ``make`` if the virtualenv is active:

::

  $ make

If virtualenv isn't active then use:

::

  $ pipenv run make


Alternative Installation Way: Wheels
-------------

Install wheel package using pip:

::

  $ pip install https://github.com/pavlobornia/pgbackup/releases/download/v0.1.0/pgbackup-0.1.0-py3-none-any.whl
