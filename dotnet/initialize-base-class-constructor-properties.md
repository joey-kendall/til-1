#In order to pass constructor parameters to the base class you need to do the following

```
public class DerivedClass : BaseClass
{
    public DerivedClass(int derivedParam, String baseParam):base(baseParam)
    {
    }
}
```
