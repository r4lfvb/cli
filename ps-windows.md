# PowerShell (Windows)

**Get the current PowerShell version number**

```ps
$PSVersionTable.PSVersion
```

**Get UWP apps installed on the system**
    
```ps
Get-AppxPackage -AllUsers | Select Name, PackageFullName | Sort-Object Name
```

**Get installed Windows apps**

```ps
Get-WmiObject -Class Win32_Product | Select Name, Version, Vendor | Sort-Object Name
```

**Get top 10 processes using CPU**

```ps
Get-Process | Sort-Object 'CPU(s)' -Descending | Select-Object -First 10
```