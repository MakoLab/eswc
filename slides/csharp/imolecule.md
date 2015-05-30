``` csharp
[Class("gc", "Molecule")]
public interface IMolecule : IEntityWithLabel
{
    [Collection("gc", "hasAtom")]
    ICollection<IAtom> Atoms { get; }

    [Collection("gc", "hasResidue")]
    ICollection<IResidue> Residues { get; }
}
```
