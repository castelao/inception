================
Tunning your DOI
================

If you are somehow related to academia and write public software, you probably should record a DOI (Digital Object Identifier) for your code. The concept is the same of scientific publications, where each article has its DOI, which is associated with the ORCID of the authors. Zenodo is a convenient way to do that, and if you use that, there is a way to finetune the DOI record automatically created by Zenodo.

Some important points missed by the default procedure are the possibility to define the funding source for the project, register important contributors that are not authors, and link this project to other projects' DOI or scientific references.

FORCE11 is a great reference for data & software citation.

If this repository was useful for you, please consider to star it (somewhere in the top right).

Example
-------

The .zenodo.json in this repository is an actual example on how to write your descriptor.

title
-----

The title of the project. The equivalent of a title of an article.

ex.:

"title": "How to tune your DOI record with Zenodo"


Contributors
------------

A list with contributors.

Possible types: ContactPerson, Researcher, Sponsor, Supervisor

ex.:

"contributors": [
    {
      "type": "ContactPerson",
      "name": "Castelao, Guilherme",
      "affiliation": "Scripps Institution of Oceanography - UC San Diego",
      "orcid": "0000-0002-6765-0708"
    },
    {
      "type": "Researcher",
      "name": "Castelao, Guilherme",
      "affiliation": "Scripps Institution of Oceanography - UC San Diego",
      "orcid": "0000-0002-6765-0708"
    },
    {
      "type": "Sponsor",
      "name": "Southern California Coastal Ocean Observing System"
    },
    {
      "type": "Supervisor",
      "name": "Castelao, Guilherme",
      "affiliation": "Scripps Institution of Oceanography - UC San Diego",
      "orcid": "0000-0002-6765-0708"
    }
  ],

Creators
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

 - accepted_types: doi, ark, ean13, eissn, handle, isbn, issn, istc, lissn, lsid, purl, upc, url, urn, ads, arxiv, bibcode

 - relation: cites, isSupplementTo

It looks like we can't add manually isVersionOf the project doi. But it is added by them automatically

ex.:

"related_identifiers": [
        {
            "scheme": "url",
            "identifier": "https://github.com/castelao/inception/tree/v0.0.3",
            "relation": "isSupplementTo"
        },
        {
            "scheme": "doi",
            "identifier": "10.21105/joss.02063",
            "relation": "cites"
        }
    ]
