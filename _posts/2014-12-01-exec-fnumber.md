---
category: Retrieving Query Result Information
apipath: '/exec/fnumber'
title: 'Return the column number associated with the given column name'
type: 'FNUMBER'

layout: null
---

 FNUMBER Returns the column number associated with the given column name.

 Usage: fnum=pgmex('fnumber',pgResult,colName)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
     colName: char [1,N] - column name
 OUTPUT:
   regular:
     fnum: double [1,1] - column number. -1 is returned if the given name
         does not match any column.

 The given name is treated like an identifier in an SQL command, that is,
 it is downcased unless double-quoted.

 Examples:

 res=pgmex('exec',dbConn,'SELECT 1 AS FOO, 2 AS "BAR"');

 name=pgmex('fname',res,0)             % foo
 name=pgmex('fname',res,1)             % BAR
 ind=pgmex('fnumber',res,'FOO')        % 0
 ind=pgmex('fnumber',res,'foo')        % 0
 ind=pgmex('fnumber',res,'BAR')        % -1
 ind=pgmex('fnumber',res,'"BAR"')      % 1