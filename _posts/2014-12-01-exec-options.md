---
category: Connection Status Functions
apipath: '/exec/options'
title: 'OPTIONS Returns the command-line options passed in the connection request'
type: 'OPTIONS'

layout: null
---

 OPTIONS Returns the command-line options passed in the connection request.

 Usage: options=pgmex('options',dbConn)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - C pointer to a PGconn structure
 OUTPUT:
   regular:
     options: char [1,N] - connection options
