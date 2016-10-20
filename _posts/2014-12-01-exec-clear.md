---
category: Command Execution Functions
apipath: '/exec/clear'
title: 'Free the storage associated with PGresult'
type: 'CLEAR'

layout: null
---

 CLEAR Frees the storage associated with a PGresult.

 Usage: pgmex('clear',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure

 Every command result should be freed via CLEAR when it is no longer
 needed.