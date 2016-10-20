---
category: Retrieving Query Result Information
apipath: '/exec/binarytuples'
title: 'Check if PGresult contains binary data or text'
type: 'BINARYTUPLES'

layout: null
---

 BINARYTUPLES Returns 1 if the PGresult contains binary data and 0 if it
 contains text data.

 Usage: isBinary=pgmex('binarytuples',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     isBinary: double [1,1] - 1 only if all columns of the result are
         binary, otherwise 0.