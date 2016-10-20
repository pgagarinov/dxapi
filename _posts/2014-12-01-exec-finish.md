---
category: Database Connection Control Functions
apipath: '/exec/finish'
title: 'Close the connection to the server'
type: 'FINISH'

layout: null
---

 FINISH Closes the connection to the server. Also frees memory used by the
 PGconn object.

 Usage: pgmex('finish',dbConn)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - C pointer to a PGconn structure

 The PGconn pointer must not be used again after PQfinish has been called.