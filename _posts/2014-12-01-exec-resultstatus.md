---
category: Command Execution Functions
apipath: '/exec/resultstatus'
title: 'Return the result status of the command'
type: 'RESULTSTATUS'

layout: null
---

 RESULTSTATUS Returns the result status of the command.

 Usage: execStatus=pgmex('resultstatus',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     execStatus: double [1,1] - result status code - see PQresultStatus at
         http://www.postgresql.org/docs/9.4/static/libpq-exec.html (status
         codes range from 0 to 9 in the order they are listed).