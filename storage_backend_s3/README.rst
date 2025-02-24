==================
Storage Backend S3
==================

.. !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-LGPL--3-blue.png
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fstorage-lightgray.png?logo=github
    :target: https://github.com/OCA/storage/tree/14.0/storage_backend_s3
    :alt: OCA/storage
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/storage-14-0/storage-14-0-storage_backend_s3
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runbot-Try%20me-875A7B.png
    :target: https://runbot.odoo-community.org/runbot/275/14.0
    :alt: Try me on Runbot

|badge1| |badge2| |badge3| |badge4| |badge5| 

Add the possibility to store and get data from amazon S3 for your storage backend

**Table of contents**

.. contents::
   :local:

Configuration
=============

Go to "Technical -> Storage backend -> Storage backend" and create a new backend of type "Amazon S3".


Example of configuration via env
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
::

  [storage_backend.name_of_your_backend]
  backend_type=amazon_s3
  served_by=external
  base_url=https://your.cdn.domain.com
  directory_path=foo  # if you want to store in this folder
  url_include_directory_path=1  # if you want to include the above folder in the URL
  aws_bucket=your-bucket-name
  aws_file_acl=public-read
  aws_access_key_id=$SECRET
  aws_secret_access_key=$MORESECRET
  aws_region=eu-central-1

Known issues / Roadmap
======================

There is an issue with the latest version of `boto3` and `urllib3`
- boto3 needs to be `boto3<=1.15.18` related with https://github.com/OCA/storage/issues/67

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/storage/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed
`feedback <https://github.com/OCA/storage/issues/new?body=module:%20storage_backend_s3%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Akretion

Contributors
~~~~~~~~~~~~

* Sebastien Beau <sebastien.beau@akretion.com>
* Raphaël Reverdy <raphael.reverdy@akretion.com>
* Simone Orsi <simone.orsi@camptocamp.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/storage <https://github.com/OCA/storage/tree/14.0/storage_backend_s3>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
