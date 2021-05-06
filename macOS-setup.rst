.. _macOS_setup:

macOS setup
===========

ssh connection to VM
--------------------

You can open your terminal and ssh-login to the Quantum Mobile VM by

::

   % ssh 127.0.0.1 -p 2222 -l max

where the password is ``moritz``.

X forwarding
------------

X forwarding via ssh is useful to open graphical tools in Quantum
Mobule to display it on your computer. For this you need to install
XQuartz. This is downloaded at https://www.xquartz.org/.

X forwarding is activated with ``-X`` or ``-Y`` option of ssh::

   % ssh 127.0.0.1 -p 2222 -l max -Y

Save ssh long setting to ``.ssh/config``
----------------------------------------

All above settings are integrated into a ``.ssh/config`` like::

   Host aiidatutorial
      Hostname 127.0.0.1
      Port 2222
      User max
      IdentityFile ~/.ssh/aiida_tutorial
      ForwardX11 yes
      ForwardX11Trusted yes
      LocalForward 8888 localhost:8888
      LocalForward 5000 localhost:5000
      ServerAliveInterval 120

Then you can login by

::

   % ssh aiidatutorial

Here ``aiidatutorial`` is the nickname and can be modified even shorter
name.
