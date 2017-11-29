===============
AWS Cost Report
===============

Simple script to generate a TSV file using the AWS Cost Explorer API.

Usage:

.. code-block:: bash

    $ # login to consolidated billing account
    $ pip3 install -U boto3
    $ ./aws-cost-and-usage-report.py --days=7 >> results.tsv
