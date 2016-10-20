---
category: Command Execution Functions
apipath: '/exec/pqexec'
title: 'Submit a command to the server and waits for the result (libpq version)'
type: 'PQEXEC'

layout: null
---

 PQEXEC Submits a command to the server and waits for the result (libpq
 version).

 Usage: pgResult=pgmex('pqexec',dbConn,command)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - C pointer to a PGconn structure
     command: char [1,N] - SQL command to be executed
 OUTPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure

 Notes:
   1) This function returns text results, which makes it unsuitable for
     some GETF requests. It is left for backwards compatibility.
   2) Unlike EXEC and PARAMEXEC, the command can contain multiple SQL
     statements separated by semicolons.
