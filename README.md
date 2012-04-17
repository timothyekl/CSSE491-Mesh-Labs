# CSSE491 (Mesh Networking) Labs

This folder contains the revised labs for CSSE491 (Mesh Networking) 
as of spring quarter 2012. All labs were created by Tim Ekl.

These labs require:

 - A working LaTeX installation
 - GNU Make
 - The following LaTeX packages: array, mdwlist, fancyhdr, color,
   graphicx, minted, fullpage, hyperref, textcomp, totcount
   
   Of these, only minted is nonstandard; it requires the Python
   package pygments. These dependencies can be found at:
   
    - http://pygments.org/
    - http://code.google.com/p/minted/

## Building a lab

For all labs, the following targets are common:

- `make all` (or simply `make`) produces all possible PDFs and packages
  for the lab.
- `make clean` removes all built and temporary files for the lab.
