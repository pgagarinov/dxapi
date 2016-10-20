---
category: Retrieving Query Result Information
apipath: '/exec/nfields'
title: 'Return the number of the query result columns'
type: 'NFIELDS'

layout: null
---

 NFIELDS Returns the number of columns (fields) in each row of the query
 result.

 Usage: nFields=pgmex('nfields',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     nFields: double [1,1] - the number of fields