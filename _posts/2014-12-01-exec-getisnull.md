---
category: Retrieving Query Result Information
apipath: '/exec/getisnull'
title: 'Test a field for a null value'
type: 'GETISNULL'

layout: null
---

 GETISNULL Tests a field for a null value.

 Usage: isNull=pgmex('getisnull',pgResult,rowInd,colInd)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     rowInd: double [1,1] - row number (starts with 0)
     colInd: double [1,1] - column number (starts with 0)
 OUTPUT:
   regular:
     isBinary: double [1,1] - 1 if the field is null and 0 if it contains
         a non-null value.