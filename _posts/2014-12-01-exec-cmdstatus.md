---
category: Retrieving Other Result Information
apipath: '/exec/cmdstatus'
title: 'Return the command status tag'
type: 'CMDSTATUS'

layout: null
---

 CMDSTATUS Returns the command status tag from the SQL command that
 generated the PGresult.

 Usage: statusStr=pgmex('cmdStatus',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     statusStr: char [1,N] - command status tag

 Commonly this is just the name of the command, but it might include
 additional data such as the number of rows processed.