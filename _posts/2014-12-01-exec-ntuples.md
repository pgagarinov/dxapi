---
category: Retrieving Query Result Information
apipath: '/exec/ntuples'
title: 'Return the number of rows (tuples) in the query result'
type: 'NTUPLES'

layout: null
---

 NTUPLES Returns the number of rows (tuples) in the query result.

 Usage: nTuples=pgmex('ntuples',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     nTuples: double [1,1] - the number of tuples

 Because the underlying libpq function returns a 32-bit integer result,
 large result sets might overflow the return value.