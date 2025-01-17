---
title: MPI_Comm_connect function
TOCTitle: MPI_Comm_connect function
ms:assetid: 17d7fb2f-18cf-4154-bc73-7005c8bce57a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473259(v=VS.85)
ms:contentKeyID: 59360805
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_CONNECT
- mpif/MPI_Comm_connect
- mpi/MPI_COMM_CONNECT
dev_langs:
- C++
- C
description: Learn how to use the MPI_Comm_connect function to form a new intercommunicator. Includes syntax, parameters, and return values.
---

# MPI\_Comm\_connect function

Make a request to form a new intercommunicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_connect(
  _In_  char     *port_name,
        MPI_Info info,
        int      root,
        MPI_Comm comm,
  _Out_ MPI_Comm *newcomm
);
```

## Parameters

  - *port\_name* \[in\]  
    Network address, used only on *root*.

  - *info*  
    Implementation-dependent information.

  - *root*  
    Rank in *comm* of root node.

  - *comm*  
    Intracommunicator over which call is collective.

  - *newcomm* \[out\]  
    Intercommunicator with server as remote group.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_CONNECT(PORT_NAME, INFO, ROOT, COMM, NEWCOMM, IERROR)
        CHARACTER*(*) PORT_NAME
        INTEGER INFO, ROOT, COMM, NEWCOMM, IERROR
```

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Mpi.h;
Mpif.h</td>
</tr>
<tr class="odd">
<td><p>Library</p></td>
<td>Msmpi.lib</td>
</tr>
<tr class="even">
<td><p>DLL</p></td>
<td>Msmpi.dll</td>
</tr>
</tbody>
</table>


## See also

[MPI Process Management Functions](mpi-process-management-functions.md)

