# PowerShell (Windows)

**Get UWP apps installed on the system**
    
```PowerShell
Get-AppxPackage -AllUsers | Select Name, PackageFullName | Sort-Object Name
```

**Get installed Windows apps**

```PowerShell
Get-WmiObject -Class Win32_Product | Select Name, Version, Vendor | Sort-Object Name
```

**Get top 10 processes using CPU**

```PowerShell
Get-Process | Sort-Object 'CPU(s)' -Descending | Select-Object -First 10
```