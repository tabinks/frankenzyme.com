---
layout: default
title: apc113179 - HLB5
project: true
---

Crystallography: Changsoo Chan project.
Goal:            Identify cellulase active site.

[cellulales-in-pdb.txt](cellulases-in-pdb.txt)

Assay Results
=============
- Carboxymethylcellulose was used a substrate in assay by Matthias Hess.  Putatative Endoglucanase.
- Acid-pretreated Miscanthus (real cellulose) showed activity but was not pegged as potential cellobiohydrolases

Endoglucanases in the PDB
=============================
- 3qxf (apo)
- 3qxq [cellopentaose](http://www.rcsb.org/pdb/ligand/ligandsummary.do?hetId=CE5&sid=3QXQ)

Cellopentaose in PDB
====================
- 2eex
- 3a8e
- 3f5k
- 3pl3
- 3qxq
- 3scu
- 4jcw


Surface Screen run 
==================

    python "/Users/tbinkowski/Box Sync/xScripts/Proteinworks/bin/screen_sdistribution.py" pocket0_atm.pdb 0 "/Users/tbinkowski/Box Sync/xScripts/Proteinworks/bin/surface-library_test_2014-07-23.json" PREFIX
    
# Date:      2014-07-23 13:12
# Running:   /Users/tbinkowski/Box Sync/xScripts/Proteinworks/bin/screen_sdistribution.py
# Machine:   tbinkowski2.sbc.anl.gov
# CPU count: 24
# Query:     pocket0_atm.pdb
# Library:   /Users/tbinkowski/Box Sync/xScripts/Proteinworks/bin/surface-library_test_2014-07-23.json (274962)
Parallel time: 1995.660956
