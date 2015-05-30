... and it's corresponding SPARQL query

``` sql
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
SELECT ?s ?p ?o ?Gmolecule0 ?molecule0
WHERE
{
    GRAPH ?Gmolecule0 {
        ?molecule0 a <http://purl.org/gc/Molecule> .
        ?molecule0 <http://purl.org/gc/hasAtom> ?atoms0 .
        ?s ?p ?o .
    }
    GRAPH <meta://graph/> { ?Gmolecule0 <http://xmlns.com/foaf/0.1/primaryTopic> ?molecule0 . }
    GRAPH ?Gatoms0 {
        ?atoms0 a <http://purl.org/gc/Atom> .
        ?atoms0 <http://purl.org/gc/isElement> ?element0 .
        FILTER(?element0 = "O"^^xsd:string)  .
        ?atoms0 <http://purl.org/gc/hasBond> ?bonds0 .
    }
    GRAPH ?Gbonds0 {
        ?bonds0 a <http://purl.org/gc/NormalBond> .
        FILTER(?bonds0 = ?bonds1)
    }
    GRAPH ?Ganother1 {
        ?another1 a <http://purl.org/gc/Molecule> .
        ?another1 <http://purl.org/gc/hasAtom> ?atoms1 .
    }
    GRAPH ?Gatoms1 {
        ?atoms1 a <http://purl.org/gc/Atom> .
        ?atoms1 <http://purl.org/gc/isElement> ?element1 .
        FILTER(?element1 = "H"^^xsd:string)  .
        ?atoms1 <http://purl.org/gc/hasBond> ?bonds1 .
    }
    GRAPH ?Gbonds1 {
        ?bonds1 a <http://purl.org/gc/NormalBond> .
        FILTER(?bonds0 = ?bonds1)
    }
}
```
