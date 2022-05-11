# PowerShell (Windows)

**Create a new GUID**

```PowerShell
[guid]::newguid()
```

**Show the PATH environment variable**

```PowerShell
$Env:Path
```

**Reload the PATH in the current session**
```PowerShell
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")
```

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
