.. title: kerl : Tool for Erlang/OTP version management
.. slug: kerl-tool-for-erlangotp-version-management
.. date: 2017-05-11 16:17:07 UTC+05:30
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text

Like rvm for Ruby and virtualenv for Python we have now kerl for Erlang/OTP.
kerl allows to install and manage multiple OTP versions. kerl is written as
a shell script and does not depend on Erlang.

The Github Repo is  https://github.com/yrashk/kerl

* Installing kerl

.. code-block:: bash

    $ cd /usr/local/bin
    $ sudo curl -O https://raw.githubusercontent.com/yrashk/kerl/master/kerl
    $ sudo chmod a+x kerl

* List available releases

.. code-block:: bash

    $ kerl list releases

* Update list of available releases

.. code-block:: bash

    $ kerl update releases

* Build a release

.. code-block:: bash

    $ kerl  build  17.0  myotp_17_0

* Listing available builds

.. code-block:: bash

    $ kerl  list builds

* Installing a build

.. code-block:: bash

    $ mkdir -p /home/me/my_otp_installations/17_0
    $ kerl  install myotp_17_0 /home/me/my_otp_installations/17_0

* Listing installations

.. code-block:: bash

    $ kerl list installations

* Use/activate a version of OTP

.. code-block:: bash

    $ source /path/to/installation/dir/activate
    $ # Example
    $ source /home/me/my_otp_installations/17_0/activate

* Deactivate/stop using for now, a version of OTP

.. code-block:: bash

    $ kerl_deactivate

* Find out which OTP version is active

.. code-block:: bash

    $ kerl active

* Get details kerl installation

.. code-block:: bash

    $ kerl status

* Delete a build

.. code-block:: bash

    $ kerl delete build myotp_17_0
