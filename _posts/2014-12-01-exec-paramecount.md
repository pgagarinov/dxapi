---
category: Working with parameters
apipath: '/exec/paramcount'
title: 'Return the number of parameters in a PGparam object'
type: 'PARAMCOUNT'

layout: null
---

 PARAMCOUNT Returns the number of parameters in a PGparam object.

 Usage: nParams=pgmex('paramcount',pgParam)

 INPUT:
   regular:
     pgParam: uint32 or uint64 [1,1] - C pointer to a PGparam structure
 OUTPUT:
   regular:
     nParams: int32 [1,1] - the number of parameters in pgParam
