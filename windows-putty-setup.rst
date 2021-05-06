.. _windows_putty_setup:

Windows PuTTY setup
===================

Installation of PuTTY
---------------------

PuTTY is downloaded at `PuTTY SSH client <https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html>`_.

To setup ``aiidatutorial`` settion of PuTTY:

-  Put the given IP address ``127.0.0.1`` at "Host Name (or IP
   address)", type ``aiidatutorial`` in the box just below "Saved
   Sessions" and click "Save".
-  Go to Connection > Data and put ``max`` as autologin username.
-  Go to Connection > SSH > Tunnels, type ``8888`` in the
   "Source Port" box, type ``localhost:8888`` in "Destination" and click "Add".
-  Repeat the previous step for port ``5000`` instead of ``8888``.
-  Go to Connection > SSH > X11, check "Enable X11 forwarding"
-  Go back to the "Session" screen, select "aiidatutorial" and click "Save"
-  Finally, click "Open" (and click "Yes" on the putty security alert
   to add the VM to your known hosts).
   You should be redirected to a bash terminal on the virtual machine.

.. note::

    Next time you open PuTTY, select ``aiidatutorial`` and click "Load" before clicking "Open".


X forwarding
------------

X forwarding via ssh is useful to open graphical tools in Quantum
Mobule to display it on your computer. For this you need to install
VcXsrv. This is downloaded at
https://sourceforge.net/projects/vcxsrv/. After the installation, open
VcXsrv once and just clicking next, next, ..., then to resident and
the icon (X mark) would appear at taskbar notification area.
