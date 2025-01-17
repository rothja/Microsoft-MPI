---
title: MPI_Type_free function
TOCTitle: MPI_Type_free function
ms:assetid: b2e32753-cd32-442e-bb67-1d3c2d417174
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520566(v=VS.85)
ms:contentKeyID: 59361037
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_FREE
- mpif/MPI_Type_free
- mpi/MPI_TYPE_FREE
dev_langs:
- C++
- C
description: Learn about the MPI_Type_free function on Microsoft's official site. Understand its syntax, parameters, return values, and related MPI Datatype Functions.
---

# MPI\_Type\_free function

Frees the datatype.

## Syntax

``` c++
int MPIAPI MPI_Type_free(
   _Inout_ MPI_Datatype *datatype
);
```

## Parameters

  - *datatype*  
    Datatype that is freed.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_FREE(DATATYPE, IERROR)
        INTEGER DATATYPE, IERROR
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

[MPI Datatype Functions](mpi-datatype-functions.md)

