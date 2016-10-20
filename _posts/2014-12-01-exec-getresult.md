---
category: Asynchronous Command Processing
apipath: '/exec/getresult'
title: 'Return a result from an asynchronous request (blocking)'
type: 'GETRESULT'

layout: null
---

 GETRESULT Waits for the next result from a prior asynchronous request,
 and returns it.

 Usage: pgResult=pgmex('getResult',dbConn)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - C pointer to a PGconn structure
 OUTPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure

 This function is of no use without other asynchronous command functions