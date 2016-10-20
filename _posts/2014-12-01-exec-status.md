---
category: Connection Status Functions
apipath: '/exec/status'
title: 'STATUS Returns the status of the connection'
type: 'STATUS'

layout: null
---

 STATUS Returns the status of the connection.

 Usage: connStatus=pgmex('status',dbConn)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - C pointer to a PGconn structure
 OUTPUT:
   regular:
     connStatus: double [1,1] - connection status code (see below)

 The status can be one of a number of values. However, only two of these
 are seen outside of an asynchronous connection procedure: CONNECTION_OK
 (0) and CONNECTION_BAD (1). A good connection to the database has the
 status CONNECTION_OK. A failed connection attempt is signaled by status
 CONNECTION_BAD. Ordinarily, an OK status will remain so until FINISH, but
 a communications failure might result in the status changing to
 CONNECTION_BAD prematurely. In that case the application could try to
 recover by calling RESET.