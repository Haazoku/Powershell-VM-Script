# Powershell-VM-Script
Powershell Script for creating a VM using PowerCLI *In vmware vSphere*

To use this you have to install PowerCLI in Powershell
        To install PowerCLI you have to input these commands:
                      
                      find-module vmware.powercli
                      install-module vmware.powercli
                      
If you have an invalid certificate or none at all (I believe it's normal to not have one), you'll have to input this command:
                      
                      Set-PowerCLIConfiguration -InvalidCertificateAction Ignore -Confirm:$false
                      
This Script was created by me from a video on how to create VMs from Powershell Commands

Video: https://www.youtube.com/watch?v=nPkYeKDeYlY
