``` csharp
[Class("gc", "Atom")]
public interface IAtom : IEntityWithLabel, IEntityWithName
{
    [Property("gc", "isElement")]
    string Element { get; set; }

    [Property("gc", "hasCoordinates")]
    IVectorValue Coordinates { get; set; }

    [Collection("gc", "hasBond")]
    IEnumerable<IBond> Bonds { get; }
}
```
