Few C# data contracts

``` csharp
[Class("gc", "MolecularSystem")]
public interface IMolecularSystem : IEntityWithLabel
{
    [Property("dcterms", "isPartOf")]
    IComputationalChemistryPublication Publication { get; set; }

    [Property("gc", "hasSystemCharge")]
    IFloatValue SystemCharge { get; set; }

    [Property("gc", "hasSystemMultiplicity")]
    IIntegerValue Multiplicity { get; set; }

    [Collection("gc", "holds")]
    IEnumerable<IMolecule> Holds { get; }
}
```
