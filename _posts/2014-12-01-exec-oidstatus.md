---
category: Retrieving Other Result Information
apipath: '/exec/oidstatus'
title: 'Return the OID of the inserted row'
type: 'OIDSTATUS'

layout: null
---

 OIDSTATUS Returns the OID of the inserted row.

 Usage: oidStr=pgmex('oidStatus',pgResult)

 INPUT:
   regular:
     pgResult: uint32 or uint64 [1,1] - C pointer to a PGresult structure
 OUTPUT:
   regular:
     oidStr: char [1,N] - a string with the OID of the inserted row.

 This function is deprecated in favor of PQoidValue and is not thread-safe.

 Returns the OID of the inserted row, if the SQL command was an INSERT
 that inserted exactly one row into a table that has OIDs, or a EXECUTE of
 a prepared query containing a suitable INSERT statement. Otherwise, this
 function returns InvalidOid. This function will also return InvalidOid if
 the table affected by the INSERT statement does not contain OIDs.