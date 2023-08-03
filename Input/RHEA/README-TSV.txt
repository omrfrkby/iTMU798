Rhea TSV files
=============================================================================

Tab-separated values is a plain text format widely used and supported, easily
imported as a spreadsheet by office packages.

Rhea cross references to other databases are exported as TSV files named
rhea2<db>.tsv, <db> being the referenced database. Each line in the file
contains the following information:
    - RHEA_ID: the Rhea unique identifier for the reaction.
    - DIRECTION: the directionality of the reaction (LR, RL, BI or UN).
    - MASTER_ID: the Rhea ID of the corresponding 'master' reaction (the
      equivalent reaction of undefined direction).
    - ID: the ID/accession referenced in the external database.
    
The file rhea2xrefs.tsv contains all of the cross references, with one more
column:
    - DB: the referenced database.

Please note that UniProt, Reactome and MACiE are automatic cross references.
Other databases are manually linked to Rhea.
