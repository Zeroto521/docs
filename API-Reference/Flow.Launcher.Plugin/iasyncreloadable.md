# IAsyncReloadable

Namespace: Flow.Launcher.Plugin

This interface is to indicate and allow plugins to asyncronously reload their
 in memory data cache or other mediums when user makes a new change
 that is not immediately captured. For example, for BrowserBookmark and Program
 plugin does not automatically detect when a user added a new bookmark or program,
 so this interface's function is exposed to allow user manually do the reloading after 
 those new additions.
 
 The command that allows user to manual reload is exposed via Plugin.Sys, and
 it will call the plugins that have implemented this interface.

```csharp
public interface IAsyncReloadable
```

## Methods

### **ReloadDataAsync()**



```csharp
Task ReloadDataAsync()
```

#### Returns

[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task)<br>
