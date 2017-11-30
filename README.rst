===============
AWS Cost Report
===============

Simple example script to generate a TSV file using the `AWS Cost Explorer API <https://aws.amazon.com/blogs/aws/new-interactive-aws-cost-explorer-api/>`_.

Usage:

.. code-block:: bash

    $ # login to consolidated billing account
    $ pip3 install -U boto3
    $ ./aws-cost-and-usage-report.py --days=7 >> results.tsv

The ``results.tsv`` file can be opened in your favorite spreadsheet application. Its contents look like:

========== ============= ====================================== ====== ==== =========
TimeSpan   LinkedAccount Service                                Amount Unit Estimated
========== ============= ====================================== ====== ==== =========
2017-10-29 123123123123  AWS CloudTrail                         12.34  USD  False
2017-10-30 123123123123  ...                                    24.50  USD  False
...
2017-11-27 001111111111  AWS CloudTrail                         0      USD  True
2017-11-27 001111111111  AWS Key Management Service             0.3336 USD  True
2017-11-27 001111111111  Amazon Elastic Compute Cloud - Compute 411.25 USD  True
2017-11-27 001111111111  Amazon Elastic Load Balancing          16.201 USD  True
========== ============= ====================================== ====== ==== =========
