=========
Weekdate
=========
.. _`weekdate`:

When preparing invoices, there's some benefit in quickly finding the dates of Monday and Sunday for a given week.  For those that prefer to write their invoices from a console-based text editor, (read: vim), Weekdate provides you with the means of quickly prepopulating a file with the dates you need to cover.

------------
Installation
------------
.. _`install`:

To install Weekdate, run the following command:

.. code-block:: console

   $ python3 setup.py install --user

This installs the weekdate script in the ``bin`` folder of your home directory.  The path to this folder can vary, but on Linux systems it is often at ``~/.local/bin``.  Once it is installed, you can call the ``weekdate`` script from the terminal.

------
Usage
------
.. _`usage`:

You can use Weekdate from the command-line.  By running the command without arguments, it provides the Monday and Sunday dates for the current week.

.. code-block:: console

   $ weekdate
   [Jul 18 - Jul 24]

Using the ``--start-date`` and ``--end-date`` parameters, you can define the start and end dates of the range you need.  Weekdate requires that pass dates in YYYY-MM-DD format.  Note that these dates default to the current date.  The starting and ending dates can be at any point in the week you want dates from.  For instance,

.. code-block:: console

   $ weekdate --start-date 2016-07-01
   [Jun 27 - Jul 03]
   [Jul 04 - Jul 10]
   [Jul 11 - Jul 17]
   [Jul 18 - Jul 24]

You may find this script most useful by redirecting its output to file.  This then gives you a base set of dates to work from when writing invoices or other records that require you to provide start and end dates.
