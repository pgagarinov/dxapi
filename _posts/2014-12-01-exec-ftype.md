---
category: Retrieving Query Result Information
apipath: '/exec/ftype'
title: 'Return the data type associated with the given column number'
type: 'FTYPE'

layout: null
---

 FTYPE Returns the data type associated with the given column number.

 Usage: ftype=pgmex('ftype',pgResult,colInd)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     colInd: double [1,1] - column number (numbers start at 0)
 OUTPUT:
   regular:
     ftype: double [1,1] - internal OID number of the type.