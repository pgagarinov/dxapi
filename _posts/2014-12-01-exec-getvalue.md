---
category: Retrieving Query Result Information
apipath: '/exec/getvalue'
title: 'Return a single field value of one row of a PGresult'
type: 'GETVALUE'

layout: null
---

 GETVALUE Returns a single field value of one row of a PGresult.

 Usage: valueStr=pgmex('getvalue',pgResult,rowInd,colInd)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     rowInd: double [1,1] - row number (starts with 0)
     colInd: double [1,1] - column number (starts with 0)
 OUTPUT:
   regular:
     value: double or char [M,N] - a numeric or a string representation of
         the field value.

 This function is deprecated: use GETF instead.

 Only text results can be handled.

 Numeric values are converted to double and returned as sclars or arrays
 of matching dimensions (up to two dimensions). The following numeric
 types are supported: smallint, integer, bigint, real, and double
 precision.

 A 1D array of 'text' is returned as a NULL-padded 2D string array.

 All other results are returned in their string representation, as
 returned by PQgetvalue
 (http://www.postgresql.org/docs/9.4/static/libpq-exec.html#LIBPQ-PQGETVALUE)