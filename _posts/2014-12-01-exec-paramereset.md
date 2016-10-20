---
category: Working with parameters
apipath: '/exec/paramreset'
title: 'PARAMRESET Clears out any previously put parameters'
type: 'PARAMRESET'

layout: null
---

 PARAMRESET Clears out any previously put parameters.

 Usage: pgmex('paramreset',pgParam)

 INPUT:
   regular:
     pgParam: uint32 or uint64 [1,1] - C pointer to a PGparam structure

 This function only resets the parameter counter, but does not free any
 memory. It is useful for reusing the PGparam object. You must still call
 PARAMCLEAR in the end.