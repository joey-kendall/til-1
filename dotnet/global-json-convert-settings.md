# To set global json serialize configuration to use camelcase serializer

## Place the following in the startup Configure method

```
JsonConvert.DefaultSettings = () => new JsonSerializerSettings
{
    ContractResolver = new CamelCasePropertyNamesContractResolver()
};
```
