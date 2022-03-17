# PDB (Program Database) 
## Introduction
The Program Database (PDB) format is a propietary file format by Microsoft for storing debugging information. Typically to access this information you would use DIA or DbgEng, however for an unreleased project, I was after a more portable solution so started developing a parser from scratch.

There is some documentation available (LLVM) and a source code dump by Microsoft, however it can be hard to follow or incomplete. This write up provide another picture of how the PDB format is constructed with some worked examples.

It is worth noting that the [LLVM](https://llvm.org/docs/PDB/index.html) documentation and the [Microsoft PDB Repo](https://github.com/microsoft/microsoft-pdb) are really valuable resources to look through. Where I can/remember I'll link to the source code files in the [Microsoft PDB Repo](https://github.com/microsoft/microsoft-pdb) for clarity.

## Goals
The initial goals of the parser were to:
* Extract function/symbol names at all offsets
* Allow me to extract type information
* Be relatively performant


## PDB Internals
The first concept in a PDB is the Multistream File (MSF) which is defined in [msf.cpp](https://github.com/microsoft/microsoft-pdb/blob/master/PDB/msf/msf.cpp). 

CARRY ON HERE.


### Multistream Fie (MSF)





## Reading and Understanding the Microsoft Source Code

## Useful Refernces
* [LLVM](https://llvm.org/docs/PDB/index.html)
* [Microsoft PDB Repo](https://github.com/microsoft/microsoft-pdb)
* [PDBParse Repo](https://github.com/moyix/pdbparse/tree/master/pdbparse)
