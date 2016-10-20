---
category: Command Execution Functions
apipath: '/exec/resulterrormessage'
title: 'Return the error message for the last command'
type: 'RESULTERRORMESSAGE'

layout: null
---

 RESULTERRORMESSAGE Returns the error message associated with the command,
 or an empty string if there was no error.

 Usage: errMsg=pgmex('resulterrormessage',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     errMsg: char [1,N] - error message

 Normally, execution commands such as EXEC throw an exception on errors.
 This command is left for backward compatibility.