---
category: Retrieving Query Result Information
apipath: '/exec/nfields'
title: 'Return the number of columns (fields) in each row of the query
 result'
type: 'FNAME'

layout: null
---

 FNAME Returns the column name associated with the given column number.

 Usage: fname=pgmex('fname',pgResult,colInd)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     colInd: double [1,1] - column number (numbers start at 0)
 OUTPUT:
   regular:
     fname: char [1,N] - column name. An empty string is returned if the
         column number is out of range.