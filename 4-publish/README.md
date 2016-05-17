# dotnet publish to IIS

* open Pipeline demo

* Add:
```
"Microsoft.AspNetCore.Server.IISIntegration": "1.0.0-rc2-*",
```
```
"tools": {
	"Microsoft.AspNetCore.Server.IISIntegration.Tools": {
	    "version": "1.0.0-*",
		"imports": "portable-net45+wp80+win8+wpa81+dnxcore50"
	}
},
"scripts": {
	"postpublish": "dotnet publish-iis --publish-folder %publish:OutputPath% --framework %publish:FullTargetFramework%"
}
```

Configure IIS