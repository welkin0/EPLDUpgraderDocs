.. _install:

Install
=======

The ACI EPLDUpgrader app can be installed directly on the APIC as an ACI app or deployed as
a standalone application hosted on a baremetal or virtual machine.

ACI Application
---------------

The application can be deployed on the APIC. Simply download the .aci file from 
`ACI Appcenter <https://aciappcenter.cisco.com>`_ and follow the installation directions based on 
your version of code.

* `2.x Install Video Example <https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/2-x/App_Center/video/cisco_aci_app_center_overview.html>`_
* `2.x Install Instructions <https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/2-x/App_Center/developer_guide/b_Cisco_ACI_App_Center_Developer_Guide/b_Cisco_ACI_App_Center_Developer_Guide_chapter_0110.html#d7964e613a1635>`_
* `3.x Install Instructions <https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/2-x/App_Center/developer_guide/b_Cisco_ACI_App_Center_Developer_Guide/b_Cisco_ACI_App_Center_Developer_Guide_chapter_0110.html#d11320e725a1635>`_ 

.. note:: Ensure you select security domain **all** when installing on the APIC

Standalone Application
----------------------

The ``standalone`` app is one that runs on a dedicated host/VM and makes remote connections to the 
APIC opposed to running as a container on the APIC. The resources for this app are very light, 
however, some users may still prefer to preserve the APIC resources and run on dedicated machine.

To execute in ``standalone`` mode, you need a host with docker installed.  See the 
`Docker documentation <https://docs.docker.com/install/>`_ for installing docker on your host.  
Once installed, execute the following command to download the EPLDUpgrader docker image and run it:

.. code-block:: bash

    host$ docker run --name ept -p 5000:443 -d agccie/epldupgrader:latest

The command will start an instance of EPLDUpgrader with the web server running on port 
5000. Login to the web UI at `https://localhost:5000 <https://localhost:5000>`_.  See the 
 :ref:`usage` section for further details regarding how to use the app.

