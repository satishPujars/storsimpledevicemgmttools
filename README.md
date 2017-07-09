# StorSimple Device Management Tools
This project will contain scripts and other tools which can be leveraged for automating StorSimple device management.

## Steps to execute the script: 
1.  Open powershell, create a new folder & change directory to the folder.

```
      mkdir C:\scripts\StorSimpleSDKTools
      cd C:\scripts\StorSimpleSDKTools
```
    
2.  Download nuget CLI under the same folder in Step1. 
    Various versions of nuget.exe are available on nuget.org/downloads. Each download link points directly to an .exe file, so be sure to right-click and save the file to your computer rather than running it from the browser. Refer [NuGet Documentation](https://docs.microsoft.com/en-gb/nuget/).
    
```
      wget https://dist.nuget.org/win-x86-commandline/latest/nuget.exe -Out nuget.exe
```
            
3.  Download the dependent SDK

```
      C:\scripts\StorSimpleSDKTools\nuget.exe install Microsoft.Azure.Management.Storsimple8000series
      C:\scripts\StorSimpleSDKTools\nuget.exe install Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.28.3
      C:\scripts\StorSimpleSDKTools\nuget.exe install Microsoft.Rest.ClientRuntime.Azure.Authentication -Version 2.2.9-preview
```
    
4.  Download the scripts and execute.

```
      wget https://github.com/anoobbacker/storsimpledevicemgmttools/raw/master/<script-name> -Out <script-name>
      .\<scripname> -SubscriptionId <subid> -ResourceGroupName <resource group> -ManagerName <device manager> -DeviceName <device name>
```
