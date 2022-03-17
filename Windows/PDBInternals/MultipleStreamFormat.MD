# MSF: Multistream File
## Introduction
A MSF can be thought of as a filesystem within a file. It contains streams that have been split up into blocks similar to how a filing system would split files into clusters. 

**Note**: LLVM describe the unit of data in a MSF file as a *block*, however the Microsoft PDB source code likes to use the term *page* - they mean the same thing. For simplicity, I will use the term **block** here as we are dealing with blocks of data, and not pages. 

## Layout
### MSF Header (Byte 0x00)
The first part of the file is the MSF Header which starts at byte 0 of the file. In the LLVM documentation this is called "The Superblock", but in the Microsoft-PDB format this is either the [MSF_HDR](https://github.com/microsoft/microsoft-pdb/blob/master/PDB/msf/msf.cpp#L933-L944) or [BIGMSF_HDR](https://github.com/microsoft/microsoft-pdb/blob/master/PDB/msf/msf.cpp#L946-L957) structure. While this header starts at block 0, it can take up more than 1 block.









## Useful References
* [Microsoft-pdb: msf.cpp](https://github.com/microsoft/microsoft-pdb/blob/master/PDB/msf/msf.cpp)
* [LLVM: MsfFile](https://llvm.org/docs/PDB/MsfFile.html)