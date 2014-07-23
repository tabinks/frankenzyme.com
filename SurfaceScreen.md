================================================================================
================================================================================
Update Surface Library
================================================================================
================================================================================

1. Update the local PDB
================================================================================
We are using /Volumes/Alpha/BackpocketLint/ as the local version for space reasons.
You need to run it twice for some reason.

    perl /Users/tbinkowski/Box\ Sync/xScripts/pdb-syncAndExtract.pl -sync -verbose
    perl /Users/tbinkowski/Box\ Sync/xScripts/pdb-syncAndExtract.pl 

2. Generate Surfaces using FPocket
================================================================================
Walk the PDB-style directory and run FPocket on each file.  It uses the file as
it is written so you may want to preprocess it depending on needs.  

   python create_pockets.py

3. Generate Surfaces using HetContacts
================================================================================
Walks the PDB directory and uses the files as input.  It outputs the surfaces into
a separate directory (HetSurfaces).  As of now some of the atoms may not be solvent
accessible.  This could be fixed by only looking at atoms in FPocket output.

	     python create_surfaceFromHetatms.py


Generate Surface library
================================================================================
This is simply a list of all the surfaces that we want to use for comparison to
our query.  It walks the PDB-style folder hierarchy and prints the full path to 
STDOUT.  It is hardcoded to use the 'HetSurfaces' library located at /Volumes/Alpha/BackpocketLint/HetSurfaces/.

	 python create_library.py


================================================================================
================================================================================
Conduct a Suface Distribution Run
================================================================================
================================================================================
0. Clean the PDB file
   
   python /Users/tbinkowski/Box\ Sync/xScripts/Proteinworks/bin/pdb_clean.py -pdb_in apc114168-cur_out.pdb -prefix test -chains ['A']

1. Generate surface for a single file

   /Users/tbinkowski/Box\ Sync/xDevelopment/fpocket2/bin/fpocket -f pdbfile.pdb 

2. Run comparison script


   python  "/Users/tbinkowski/Box Sync/xScripts/Proteinworks/bin/screen_sdistribution.py" apc114168-cur_out/pockets/pocket0_atm.pdb  0 "/Users/tbinkowski/Box Sync/xScripts/Proteinworks/data/surface-library_2014-04-17.json" PREFIX

Perfect match is (0.0, 1.0).


Run 1
================================================================================
python screen_alignment.py /Volumes/Alpha/BackpocketLint/HetSurfaces/05/105m.HEM_A_155.pdb /Volumes/Alpha/BackpocketLint/HetSurfaces/05/105m.HEM_A_155.pdb


Performance 
3 - 13 seconds
4 - 472 seconds
5 - ???
6 - ???


Quick Visualization
--------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------

T. Andrew Binkowski, Ph.D.
Scientist, Center for Structural Genomics of Infectious Diseases, Argonne National Laboratory
Fellow, Computation Institute, The University of Chicago
Lecturer, Department of Computer Science, The University of Chicago
Email: abinkowski@uchicago.edu
Office: 630-252-3927  Fax: 630-252-6991

--------------------------------------------------------------------------------------------------------------------------------------
