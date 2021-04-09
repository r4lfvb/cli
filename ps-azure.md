# PowerShell (Azure)

**Register resource providers**

```ps
Select-AzureRmSubscription -SubscriptionName “”

# get available providers that are not registered

$providerNamespaces = @(Get-AzureRmResourceProvider -ListAvailable) | ? {$_.RegistrationState -eq “NotRegistered” } | select ProviderNamespace

# register each unregistered provider

$providerNamespaces | foreach {
    write-host $_.ProviderNamespace
    Register-AzureRmResourceProvider -ProviderNamespace $_.ProviderNamespace
}
```