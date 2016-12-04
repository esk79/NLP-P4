# qa-system
How to run code:

1. Make sure you have vagrant installed (https://www.vagrantup.com/downloads.html)
2. Make sure you have some virtualization installed (VirtualBox, VMWare, etc) ie https://www.virtualbox.org/wiki/Downloads
3. $ cd code
4. $ vagrant up (this will take a while)
5. Place the GoogleNews-vectors-negative300.bin into the qa-system folder on the host (the folders are synced so this will appear on the guest as well. We are also assuming you already have this downloaded on your host. Otherwise https://docs.google.com/uc?id=0B7XkCwpI5KDYNlNUTTlSS21pQmM&export=download)
6. $ vagrant ssh (once 'vagrant up' has completed)
7. $ cd qa-system (these commands on now form with the guest)
8. $ python Part2.py