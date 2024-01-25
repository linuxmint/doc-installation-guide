Partitioning
============

Disks and partitions under Linux
--------------------------------

If you are not familiar with the Linux naming scheme for devices and partitions, or the concept of filesystems and mount points, read:

* `A beginner’s guide to disks and disk partitions in Linux <http://linuxbsdos.com/2014/11/08/a-beginners-guide-to-disks-and-disk-partitions-in-linux/>`_
* `Device Names in Linux <https://www.debian.org/releases/bookworm/amd64/apcs04.en.html>`_
* `Understanding the Linux File System <http://etutorials.org/Linux+systems/red+hat+linux+9+professional+secrets/Part+II+Exploring+Red+Hat+Linux/Chapter+7+Red+Hat+Linux+Basics/Understanding+the+Linux+File+System/>`_

Dedicated /home partition
-------------------------

In Linux, the ``/home`` directory is used to store user data and preferences.

This directory contains one subdirectoy for each user account. Say your username is ``john``, your home directory is ``/home/john``, your downloads are in ``/home/john/Downloads``, your documents in ``/home/john/Documents``, your Firefox bookmarks somewhere in ``/home/john/.mozilla`` and so on...

By giving ``/home`` its own dedicated partition, you separate the user data from the rest of the operating system.

The advantage is that you can wipe the operating system and replace it without affecting the user data.

When installing Linux Mint:

1. Assign the ``/`` mount point to the partition dedicated to the operating system, and tell the installer to format it.

2. Assign the ``/home`` mount point to the partition dedicated to the user data, and if it contains user data already, make sure to tell the installer **not to format it**.

.. warning::
    This is not recommended for novice users. A misstep during the installation could wipe all your data. Always make backups, make sure to select the right partitions and to carefully review formatting options.

.. note::
    A Linux Mint operating system takes about 15GB and grows as you install additional software. If you can spare the size, give it 100GB. Keep most of your free space for the home partition. User data (downloads, videos, pictures) takes a lot more space.
