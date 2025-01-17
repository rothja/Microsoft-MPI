---
title: MPI_Get_count function
TOCTitle: MPI_Get_count function
ms:assetid: e464e9ce-e387-4a12-9bb1-1d500c2960be
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473380(v=VS.85)
ms:contentKeyID: 59360916
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_GET_COUNT
- mpif/MPI_Get_count
- mpi/MPI_GET_COUNT
dev_langs:
- C++
- C
description: Learn about the MPI_Get_count function on Microsoft's official site. Understand its syntax, parameters, return values, and usage in HPC Pack.
---

# MPI\_Get\_count function

Gets the number of "top level" elements.

## Syntax

``` c++
int MPIAPI MPI_Get_count(
  _In_  MPI_Status   *status,
        MPI_Datatype datatype,
  _Out_ int          *count
);
```

## Parameters

  - *status* \[in\]  
    Return status of receive operation.

  - *datatype*  
    Datatype of each receive buffer element.

  - *count* \[out\]  
    Number of received elements.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_GET_COUNT(STATUS, DATATYPE, COUNT, IERROR)
        INTEGER STATUS(MPI_STATUS_SIZE), DATATYPE, COUNT, IERROR
```

## Remarks

If the size of the datatype is zero, this routine will return a count of zero.  If the amount of data in *status* is not an exact multiple of the size of *datatype* (so that *count* would not be integral), a *count* of **MPI\_UNDEFINED** is returned instead.

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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

