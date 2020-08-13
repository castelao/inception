================
Tunning your DOI
================


title
-----

The title of the project. The equivalent of a title of an article.

ex.:

"title": "How to tune your DOI record with Zenodo"

creators
--------

A list with authors. If missing, Zenodo gets this information from Github. I'm not sure how. Probably the list of all contributors?

ex.:

"creators": [
    {
      "name": "Castelao, Guilherme",
      "affiliation": "Scripps Institution of Oceanography - UC San Diego",
      "orcid": "0000-0002-6765-0708"
    }
  ]


By including the ORCID field, the authors are automatically linked. Check my record and you'll see my open source projects: https://orcid.org/0000-0002-6765-0708

Related Identifiers
-------------------

ex.:

"related_identifiers": [
        {
            "scheme": "url",
            "identifier": "https://github.com/castelao/inception/tree/v0.0.3",
            "relation": "isSupplementTo"
        },
        {
            "scheme": "doi",
            "identifier": "10.5281/zenodo.3981501",
            "relation": "isVersionOf"
        },
        {
            "scheme": "doi",
            "identifier": "10.21105/joss.02063",
            "relation": "cites"
        }
    ]
