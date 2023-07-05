# Xeroxprintingonlinux
A quick little fix i discovered how Linux users can easily Print and configure a Xerox printer

First of all download the Files from Xerox here (in my example that is the Altalink C8100 and versalink b400, you will of course will have to download the linux drivers for your Printer):
https://www.support.xerox.com/en-us/product/altalink-c8100-series/downloads?platform=linux&product=&category=drivers&language=en&attributeId=
https://www.support.xerox.com/en-us/product/versalink-b400/downloads?platform=linux&category=&language=en&attributeId=

If you want to do it remotely over SSH here is how:

Transfer the file via SSH with the following command:
scp <file location>* username@LinuxIP:<destination folder>
Make sure there are no spaces in the path as they will not be recognized.

On the Linux machine again cd to the folder with the file and install it with "sudo apt install <file path>"
type for instance "cd /opt/XeroxOffice/prtsy"

Open the Xerox printer manager with ./xeroxofficeprtmgr

In the printer manager press on the dropdown menu in the top right.

After that name the printer (whatever)
Select Xerox Office Standard Driver
Connection type TCP/IP (Workstation to Printer)
Then the IP of the Printer
Make this my default printer.

After that ok and you should be able to print.
If you send something to print it will print immediately without the need to provide a batch if you have that configured.
