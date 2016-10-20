---
category: Command Execution Functions
apipath: '/exec/paramexec'
title: 'Submit a parameterized command to the server and waits for the result'
type: 'PARAMEXEC'

layout: null
---

PARAMEXEC Submits a parameterized command to the server and waits for the
 result (see http://libpqtypes.esilo.com/man3/PQparamExec.html)

 Usage: pgResult=pgmex('paramexec',dbConn,pgParam,commandStr)

 INPUT:
   regular:
     dbConn: uint32 or uint64 [1,1] - database connection, a C pointer
         to a PGconn structure
     pgParam: uint32 or uint64 [1,1] - C pointer to a PGparam structure
         that holds query parameters.
     commandStr: char [1,N] - SQL command to be executed
 OUTPUT:
   optional:
     pgResult: uint32 or uint64 [1,1] - query result, a C pointer to a
         PGresult structure

 Notes:
   1) Parameters can be packed into pgParam with the PUTF function.
     If the query does not reference any parameters, a null pointer
     uint32(0) or uint64(0) can be used in place of pgParam; this is
     equivalent to the EXEC command.
   2) The command can contain only a single SQL statement (nested
     function calls or complex SELECT statements are admissible).
   3) Server errors (e.g. due to malformed SQL) will trigger exceptions.
   4) If no output is requested, the result will be disposed of
     automatically. Otherwise, the result needs to be cleared using the
     CLEAR command to avoid memory leaks (even if no tuples were
     returned.)

 Example:

 param=pgmex('paramcreate',dbConn);
 pgmex('putf',param,'%int4 %name',10,'foo');
 res=pgmex('paramexec',dbConn,param,...
     'select * from my_table where ind > $1 and code = $2');
 pgmex('paramclear',param);
 % do something with result...
 pgmex('clear',res);
