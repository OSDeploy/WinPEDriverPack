# OSDeploy | WinPE DriverPack Repository
The WinPE DriverPack Repository contains many drivers that can be used in WinPE or WinRE, including integration with OSDCloud.  It is recommended that you clone this Repository to your local machine so you can easily add these Drivers when creating your WinPE Boot Image.

## OSDCloud Integration
Coming soon.

## Install Git for Windows
Ideally, you should clone this Repostiory to your local machine so you can easily add these Drivers when creating your WinPE Boot Image.  You'll want to make sure that you have Git for Windows https://gitforwindows.org/ installed.  The easy way to install Git for Windows is to use Winget.

```powershell
# Install Git for Windows using Winget
winget install -e --id Git.Git
```

Since Git for Windows needs to modify your Path, you will need to relaunch PowerShell, or run this snippet:

```powershell
function Update-EnvironmentValues {
    $locations = 'HKLM:\SYSTEM\CurrentControlSet\Control\Session Manager\Environment','HKCU:\Environment'
    $locations | ForEach-Object {   
        $k = Get-Item $_
        $k.GetValueNames() | ForEach-Object {
            $name = $_
            $value = $k.GetValue($_)
            Set-Item -Path Env:\$name -Value $value
        }
    }
}
Update-EnvironmentValues
```

## Clone the OSDeploy | WinPE DriverPack Repository
You can use the following snippet to clone the Repository to your local machine.  

```powershell
# Source Git Repository
$Source = 'https://github.com/OSDeploy/WinPEDriverPack.git'

# Destination Folder
$Destination = $env:ProgramData + "\OSDeploy\WinPEDriverPack\"

# Git Clone Reset and Clean
# This method is used to keep the Destination in sync with changes from the Source
git clone "$Source" "$Destination"
Push-Location "$Destination"
git fetch origin
git reset --hard origin/main
git clean -f -d
Pop-Location
```

## File Content

```
Root Content
Folder FileCount SizeMb
------ --------- ------
amd64       2951 998.33
arm64        728 130.26

amd64 Content
Folder                         FileCount SizeMb
------                         --------- ------
AMD                                    5   0.14
Dell                                 224  97.75
HP                                   635 125.65
Intel-Ethernet                        33  11.97
Intel-RAID                             6   1.75
Intel-Wireless                        22 122.93
Intel-Wireless-EOL                    28 146.09
Microsoft-SurfaceBook                 20   2.72
Microsoft-SurfaceBook2                31   2.23
Microsoft-SurfaceBook3                76   8.66
Microsoft-SurfaceGo                    3   0.15
Microsoft-SurfaceGo-LTE                3   0.15
Microsoft-SurfaceGo2                   3   0.12
Microsoft-SurfaceGo3                  31   2.39
Microsoft-SurfaceGo4                  51  10.21
Microsoft-SurfaceHub3                 38   9.58
Microsoft-SurfaceLaptop3              53   5.96
Microsoft-SurfaceLaptop3-AMD          50   5.29
Microsoft-SurfaceLaptop4              87   9.31
Microsoft-SurfaceLaptop4-AMD          57   6.93
Microsoft-SurfaceLaptop5              92  15.07
Microsoft-SurfaceLaptop6             106  56.27
Microsoft-SurfaceLaptopGo             50  10.97
Microsoft-SurfaceLaptopGo2            61   7.78
Microsoft-SurfaceLaptopGo3            87  13.80
Microsoft-SurfaceLaptopStudio         98  14.52
Microsoft-SurfaceLaptopStudio2       111  26.81
Microsoft-SurfacePro10                91  15.04
Microsoft-SurfacePro5                 36   3.63
Microsoft-SurfacePro5-LTE             36   3.63
Microsoft-SurfacePro6                 36   3.68
Microsoft-SurfacePro7                 51   6.24
Microsoft-SurfacePro7-Plus            88   9.24
Microsoft-SurfacePro8                 99  14.35
Microsoft-SurfacePro9                 97  15.40
Microsoft-SurfaceStudio2              24   2.78
Microsoft-SurfaceStudio2-Plus         76  10.86
RedHat                                25   2.38
USB                                   26   7.02
VMware                                13   0.34
Win11-Ethernet                        12   3.11
Win11-Wireless                       180 185.45

arm64 Content
Folder                   FileCount SizeMb
------                   --------- ------
Dell-Latitude-7455             223  44.54
Dell-XPS13-9345                223  44.53
HP-EliteBookUltra              133  13.04
Microsoft-SurfaceLaptop7        40   8.77
Microsoft-SurfacePro11          52   9.53
Microsoft-SurfacePro9           57   9.84
```