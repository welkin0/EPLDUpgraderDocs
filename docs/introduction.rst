Introduction
============

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
            src="https://www.youtube.com/embed/HIisSTBr-bw" frameborder="0" 
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen
        ></iframe>
    </div>

The EPLD Upgrader app is a Cisco ACI application that allows administrators to upgrade switch EPLD
images. The EPLD image is extracted from the user selected NXOS image, copied to the switch, and 
then used as the base EPLD for upgrade. EPLD upgrades require a board power cycle on the switch
which can be done immediately after successful upgrade or at a later time within the app.

For normal ACI fabric operation, the EPLD is upgraded when the switch is policy-upgraded. For this
reason, ACI EPLD images are not currently published on Cisco download page.  There are, however,
scenarios where user may need to upgrade EPLD image without performing a policy-based upgrade.
An example includes a software defect with EPLD fixes and user is not able to perform a full fabric
upgrade. User can download the ACI NXOS image with the EPLD fixes, and use this app to upgrade just
the switch EPLD.

