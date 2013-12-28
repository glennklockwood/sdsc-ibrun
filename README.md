SDSC ibrun
==========

`ibrun` - launch MPI jobs from an implementation-independent command

This application launches an MPI job using a simple user interface that 
automatically configures the implementation- and system-specific features on 
whichever MPI stack the user wants to use.  It also provides an 
administrator-configurable optimal set of settings as well as a best-guess 
binding policy based on job geometry.

This application was inspired by the ibrun implementation created by the
Texas Advanced Computing Center and strives to be, at minimum, functionally 
equivalent at the user level.  The SDSC version also provides additional
functionality and features which augment the core featureset.

Known Issues
------------
Currently the following features are not supported:
* MPICH2 stack
* vSMP queue and nodes (SDSC Gordon) 
* -o and -no options

The following edge cases are not necessarily handled gracefully:
* When -n is less than -N
* When -n is 1

Features to Implement
---------------------
* completely separate the option detection for user input, resource manager, 
  and internal guessing
* provide stronger unification for the -tpp and -npernode option

Author
------
This application is currently maintained by Glenn K. Lockwood at the San Diego
Supercomputer Center.
