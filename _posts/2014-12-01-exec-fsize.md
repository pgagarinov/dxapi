---
category: Retrieving Query Result Information
apipath: '/exec/fsize'
title: 'Return the size in bytes of the column associated with the given
 column number'

layout: null
---

 FSIZE Returns the size in bytes of the column associated with the given
 column number.

 Usage: fsize=pgmex('fsize',pgResult,colInd)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     colInd: double [1,1] - column number (numbers start at 0)
 OUTPUT:
   regular:
     fsize: double [1,1] - the space allocated for this column in a
         database row. A negative value indicates the data type is
         variable-length.

 This function returns the size of the server's internal representation of
 the data type. Accordingly, it is not really very useful to clients.