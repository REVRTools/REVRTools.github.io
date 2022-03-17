# PDB (Program Database) 
## Introduction
The Program Database (PDB) format is a propietary file format by Microsoft for storing debugging information. Typically to access this information you would use DIA or DbgEng, however for an unreleased project, I was after a more portable solution so started developing a parser from scratch.

There is some documentation available (LLVM) and a source code dump by Microsoft, however it can be hard to follow or incomplete. This write up provide another picture of how the PDB format is constructed with some worked examples.

It is worth noting that the [LLVM](https://llvm.org/docs/PDB/index.html) documentation and the [Microsoft PDB Repo](https://github.com/microsoft/microsoft-pdb) are really valuable resources to look through. Where I can/remember I'll link to the source code files in the [Microsoft PDB Repo](https://github.com/microsoft/microsoft-pdb) for clarity.


## PDB File Format
The first thing to understand about the PDB file is made up of various streams of data and they are all stored within a MSF (Multistream File). The index of each stream is akin to a filename and the first few indexes have special meanings and the rest are indexed from content of other streams.

* [Multistream File Details](MultipleStreamFormat.MD)

### Multistream Fie (MSF)






## Reading and Understanding the Microsoft Source Code

## Useful Refernces
* [LLVM](https://llvm.org/docs/PDB/index.html)
* [Microsoft PDB Repo](https://github.com/microsoft/microsoft-pdb)
* [PDBParse Repo](https://github.com/moyix/pdbparse/tree/master/pdbparse)
