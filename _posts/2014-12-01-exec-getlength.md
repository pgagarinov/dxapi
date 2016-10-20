---
category: Retrieving Query Result Information
apipath: '/exec/getlength'
title: 'Return a field value length (in bytes)'
type: 'GETLENGTH'

layout: null
---

 GETLENGTH Returns the actual length of a field value in bytes.

 Usage: length=pgmex('getlength',pgResult,rowInd,colInd)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     rowInd: double [1,1] - row number (starts with 0)
     colInd: double [1,1] - column number (starts with 0)
 OUTPUT:
   regular:
     length: double [1,1] - the actual data length for the particular data
         value.

 This function returns the length of the data pointed by PQgetvalue (but
 not necessarily by the MEX functions GETVALUE or GETF). It is not likely
 to be useful to clients.