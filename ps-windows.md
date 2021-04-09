# PowerShell

## Windows

**Get the current PowerShell version number**

    $PSVersionTable.PSVersion

**Get UWP apps installed on the system**
    
    Get-AppxPackage -AllUsers | Select Name, PackageFullName | Sort-Object Name

**Get installed Windows apps**

    Get-WmiObject -Class Win32_Product | Select Name, Version, Vendor | Sort-Object Name

**Get top 10 processes using CPU**

    Get-Process | Sort-Object 'CPU(s)' -Descending | Select-Object -First 10