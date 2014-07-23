---
layout: post
title: Update Surface Library
---

## Update the local PDB
We are using `/Volumes/Alpha/BackpocketLint/` as the local version for space reasons.
You need to run it twice for some reason.

```
perl /Users/tbinkowski/Box\ Sync/xScripts/pdb-syncAndExtract.pl -sync -verbose
perl /Users/tbinkowski/Box\ Sync/xScripts/pdb-syncAndExtract.pl
```
## Generate Surfaces using FPocket
Walk the PDB-style directory and run FPocket on each file.  It uses the file as
it is written so you may want to preprocess it depending on needs.  

`python create_pockets.py`

## Generate Surfaces using HetContacts
Walks the PDB directory and uses the files as input.  It outputs the surfaces into
a separate directory (HetSurfaces).  As of now some of the atoms may not be solvent
accessible.  This could be fixed by only looking at atoms in FPocket output.

`python create_surfaceFromHetatms.py`

## Generate The Surface library
This is simply a list of all the surfaces that we want to use for comparison to
our query.  It walks the PDB-style folder hierarchy and prints the full path to 
a JSON file named *surface-library_prefix_date.json*.  

It is current hardcoded to use the 'HetSurfaces' library located at `/Volumes/Alpha/BackpocketLint/HetSurfaces/`.
```
cd /Users/tbinkowski/Box\ Sync/xScripts/Proteinworks/bin
python create_library.py prefix_name
```
