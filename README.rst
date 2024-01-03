
.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.3981501.svg
   :target: https://doi.org/10.5281/zenodo.3981501

=============
Minting a DOI
=============

If you are somehow related to academia and write public software, you probably should record a DOI (Digital Object Identifier) for your code.
The concept is the same as scientific publications, where each article has its DOI, which is associated with the authors, usually through an ORCID.
Zenodo is a convenient way to do that, and there is a way to link your repository with Zenodo to automate several steps.
GitHub Guides provide a nice reference on how to set up that: https://guides.github.com/activities/citable-code/

================
Tunning your DOI
================

Zenodo automatically captures the basic metadata for the DOI record, such as title and authors. However, it can be worthy of providing more information such as: the ORCID of the authors, the published paper that this code is related to, the DOI of the dataset that this code processes, etc.
It is possible to configure some of those fields manually at Zenodo. Instead, a convenient alternative is by providing that information in a JSON file directly in the repository so that every new release, thus new DOI, Zenodo gets a complete record.

Some important points missed by the default procedure are the possibility to define the funding source for the project, register important contributors that are not authors, and link this project to other projects' DOI or scientific references.

FORCE11 is a great reference for data & software citation.

Example
-------

The .zenodo.json in this repository is an actual example on how to write your descriptor.
You can check the outcome result at https://doi.org/10.5281/zenodo.3981501

Title
-----

The title of the project. The equivalent of a title of an article.

ex.:

"title": "How to tune your DOI record with Zenodo"


License
-------

The license of the project. Check https://spdx.org/licenses/ for a list of
licenses and their abbreviations.

ex.:

"license": "MIT"

Contributors
------------

A list with contributors.

Possible types: ContactPerson, DataCollector, DataCurator, DataManager, Distributor, Editor, HostingInstitution, Other, Producer, ProjectLeader, ProjectManager, ProjectMember, RegistrationAgency, RegistrationAuthority, RelatedPerson, Researcher, ResearchGroup, RightsHolder, Sponsor, Supervisor, WorkPackageLeader

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

 - accepted_types: ads, ark, arxiv, bioproject, biosample, doi, ean13, ean8, ensembl, genome, gnd, hal, handle, isbn, isni, issn, istc, lsid, orcid, pmcid, pmid, purl, refseq, sra, uniprot, url, urn, swh, ascl

 - relation: isCitedBy, cites, isSupplementTo, isSupplementedBy, isContinuedBy, continues, hasMetadata, isMetadataFor, isNewVersionOf, isPreviousVersionOf, isPartOf, hasPart, isReferencedBy, references, isDocumentedBy, documents, isCompiledBy, compiles, isVariantFormOf, isOrignialFormOf, isIdenticalTo, isReviewedBy, reviews, isDerivedFrom, isSourceOf

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
