---
category: Retrieving Other Result Information
apipath: '/exec/cmdtuples'
title: 'Return the number of rows affected by the SQL command'
type: 'CMDTUPLES'

layout: null
---

 CMDTUPLES Returns the number of rows affected by the SQL command.

 Usage: tuplesStr=pgmex('cmdTuples',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     tuplesStr: char [1,N] - a string containing the number of rows
         affected by the SQL statement that generated the PGresult.

 This function can only be used following the execution of a SELECT,
 CREATE TABLE AS, INSERT, UPDATE, DELETE, MOVE, FETCH, or COPY statement,
 or an EXECUTE of a prepared query that contains an INSERT, UPDATE, or
 DELETE statement. If the command that generated the PGresult was anything
 else, PQcmdTuples returns an empty string.