# Linux -> Windows Reboot Automation

### What is it?
The bootswitch is a payload for a Rubber Ducky: a hacking device that emulates a keyboard to regurgitate keyboard inputs at superhuman speeds. This enables script execution if the bad usb is plugged in to the computer. The Rubber Ducky is a perfect candidate for this project because it enables automated control without needing the processes to run locally, an impossible task for UEFI navigation. So the Ducky gets plugged in, executes a series of inputs to reboot the PC into UEFI, then switches to Windows and logs in after a few minutes allocated to loading the system.

### Background
In spring of 2026 I switched to Linux because I was fed up with the bloat, the push of AI, and the lack of privacy in the Windows operating system. Unfortunately there remains a small handful of applications that I am only able to run in Windows. I consistently find myself resistant to the simple task of switching over on my dual boot, even though the process is very simple and takes only a few minutes. To solve for this I have created a Rubber Ducky payload that, when plugged in, opens a terminal, reboots into the UEFI and navigates to switch the boot order and enable secure boot, then boots into windows and logs in.

### Implementation
To use the bootswitch, first edit the configuration section (lines 4-9) based on your Linux GUI, whether you have secure boot enabled for this distro, and your motherboard brand. Then set the ```#WINDOWSPASSWORD``` constant on line 9 to your Windows PIN or password and ensure that this script remains ONLY on your Ducky, as well as that no one has access to this ducky.

Finally flash this code to your Rubber Ducky through it's supported software (Arduino IDE for most adafruit chips) and test it out!
