---
category: Working with parameters
apipath: '/exec/paramclear'
title: 'PARAMCLEAR Releases all resources being used by a PGparam object'
type: 'PARAMCLEAR'

layout: null
---

 PARAMCLEAR Releases all resources being used by a PGparam object.

 Usage: pgmex('paramclear',pgParam)

 INPUT:
   regular:
     pgParam: uint32 or uint64 [1,1] - C pointer to a PGparam structure

 The object should not be used after a clear.