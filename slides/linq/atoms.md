LINQ query for atoms matching 'O' letter

``` csharp
var atoms = from atom in entityContext.AsQueryable<IAtom>()
            where Regex.IsMatch(atom.Label, "o")
            select atom;
foreach (var atom in atoms)
{
    Console.WriteLine(atom.Label);
}
```
