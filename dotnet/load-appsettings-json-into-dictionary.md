# To load appsettings.json into dictionary you can use ToDictionary

```ConfigurationRoot.GetSection('Name').ToDictionary(x => x.Key, x => x.Value)```

Or also try

```var config =  Configuration.GetSection("MobileConfigInfo").Get<Dictionary<string, string>>(); ```


this is a test
