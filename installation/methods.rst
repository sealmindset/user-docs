Manual Installation
^^^^^^^^^^^^^^^^^^^

Manual installation of OWTF is nothing but cloning the repo and running the install script

.. code-block:: bash

    git clone https://github.com/owtf/owtf.git
    cd owtf/
    ./install/install.py

Bootstrap Script
^^^^^^^^^^^^^^^^

Using our bootstrap script automates the cloning of OWTF repo and launching install script

.. code-block:: bash

    wget https://raw.githubusercontent.com/owtf/bootstrap-script/master/bootstrap.sh
    chmod +x bootstrap.sh
    ./bootstrap.sh
