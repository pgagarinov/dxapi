---
category: Working with parameters
apipath: '/exec/paramecreate'
title: 'PARAMCREATE Creates a new PGparam object for storing command parameters'
type: 'PARAMCREATE'

layout: null
---

 PARAMCREATE Creates a new PGparam object for storing command parameters.

 Usage: pgParam=pgmex('paramcreate',dbConn)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - C pointer to a PGconn structure
 OUTPUT:
   regular:
     pgParam: uint32 or uint64 [1,1] - C pointer to a PGparam structure