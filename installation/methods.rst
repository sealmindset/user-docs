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

Alt Manual Installation
^^^^^^^^^^^^^^^^^^^^^^^

Manual installation on Kali Linux 2.0 AMD64

.. code-block:: bash

    apt-get update && apt-get upgrade -y
    apt-get dist-upgrade -y
    service postgresql start
    update-rc.d postgresql enable
    cd /opt
    git clone https://github.com/owtf/owtf.git
    pip install --upgrade cffi
    apt-get install libssl-dev
    pip install --upgrade -r /opt/owtf/install/owtf.pip
    pip install --upgrade beautifulsoup4 lxml Markdown psycopg2 pycurl six
    apt-get install libpq-dev
    chmod u+x /opt/owtf/install/install.py
    /opt/owtf/install/./install.py
    /opt/owtf/script/./db_setup.py init
    Edit /opt/owtf/profiles/general/default_backtrack.cfg
    Change the line for TOOL_METASPLOIT_DIR with /usr/share/metasploit-framework
    Edit /opt/owtf/profiles/general/default.cfg
    Change the line for TOOL_METASPLOIT_DIR with /usr/share/metasploit-framework    
    Edit /opt/owtf/profiles/general/default_backtrack.cfg
    
    NOTE: msfcli is obsolete now use msfconsole -x
    
    find /opt/owtf -type f -print0 | xargs -0 sed -i 's/msfcli /msfconsole -x /g'
