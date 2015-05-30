``` javascript
{
  "@context": {
     "foaf": "http://xmlns.com/foaf/0.1/",
     "name": "foaf:name",
     "lastName": "foaf:familyName",
     "Person": "foaf:Person",
     "interests": "http://dbpedia.org/property/interests"
  },
  "@id": "http://t-code.pl/#tomasz",
  "@type": "Person",
  "name": "Tomasz",
  "lastName": { "@value": "Pluskiewicz" },
  "interests": [ "RDF", ".NET" ]
}
```

(Other formats are transformed to JSON-LD first)