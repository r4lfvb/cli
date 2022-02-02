Commands for working with [SQL Server Express LocalDb](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/sql-server-express-localdb).

The default instance name is _MSSQLLocalDb_.

Note the path to the _SqlLocalDB.exe_ may be different depending on the version of SQL Server Express.

**Get info on the default instance of LocalDB**
```cmd
  "C:\Program Files\Microsoft SQL Server\150\Tools\Binn\SqlLocalDB.exe" info MSSQLLocalDb
```

**Create an instance of LocalDB**
```cmd
  "C:\Program Files\Microsoft SQL Server\150\Tools\Binn\SqlLocalDB.exe" create <InstanceNameHere>
```

**Start the instance of LocalDB**
```cmd
  "C:\Program Files\Microsoft SQL Server\150\Tools\Binn\SqlLocalDB.exe" start <InstanceNameHere>
```

**Stop the instance of LocalDB**
```cmd
  "C:\Program Files\Microsoft SQL Server\150\Tools\Binn\SqlLocalDB.exe" stop <InstanceNameHere>
```
See the [full reference](https://docs.microsoft.com/en-us/sql/tools/sqllocaldb-utility?view=sql-server-ver15) on using the _SqlLocalDb_ util.
