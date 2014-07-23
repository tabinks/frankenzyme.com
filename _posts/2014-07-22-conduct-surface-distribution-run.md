---
layout: post
title: Conduct a Suface Distribution Run
---

## Clean the PDB file
	
`python /Users/tbinkowski/Box\ Sync/xScripts/Proteinworks/bin/pdb_clean.py -pdb_in apc114168-cur_out.pdb -prefix test -chains ['A']`

## Generate surface for a single file

`/Users/tbinkowski/Box\ Sync/xDevelopment/fpocket2/bin/fpocket -f pdbfile.pdb`

## Run comparison script

`python  "/Users/tbinkowski/Box Sync/xScripts/Proteinworks/bin/screen_sdistribution.py" apc114168-cur_out/pockets/pocket0_atm.pdb  0 "/Users/tbinkowski/Box Sync/xScripts/Proteinworks/data/surface-library_2014-04-17.json" PREFIX`

Perfect match is (0.0, 1.0).


Run 1
================================================================================
`python screen_alignment.py /Volumes/Alpha/BackpocketLint/HetSurfaces/05/105m.HEM_A_155.pdb /Volumes/Alpha/BackpocketLint/HetSurfaces/05/105m.HEM_A_155.pdb`


Performance 
3 - 13 seconds
4 - 472 seconds
5 - ???
6 - ???
