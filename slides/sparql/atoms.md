... and it's corresponging SPARQL query

``` sql
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
SELECT ?s ?p ?o ?Gatom0 ?atom0
WHERE
{
    GRAPH ?Gatom0
    {
        ?atom0 a <http://purl.org/gc/Atom> .
        ?atom0 <http://www.w3.org/2000/01/rdf-schema#label> ?label0 .
        FILTER(REGEX(?label0,"o"))  .
        ?s ?p ?o .
    }
    GRAPH <meta://graph/>
    {
        ?Gatom0 <http://xmlns.com/foaf/0.1/primaryTopic> ?atom0 .
    }
}
```
