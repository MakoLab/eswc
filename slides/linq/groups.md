LINQ query for functional groups of type O-H

``` csharp
var groups = from molecule in entityContext.AsQueryable<IMolecule>()
    from atom in molecule.Atoms
    where atom.Element == "O"
    from bond in atom.Bonds
    from another in entityContext.AsQueryable<IMolecule>()
    from anotherAtom in another.Atoms
    where anotherAtom.Element == "H"
    from anotherBond in anotherAtom.Bonds
    where bond.Id == anotherBond.Id
    select molecule;
foreach (var group in groups)
{
    Console.WriteLine(group.Label);
}
```
