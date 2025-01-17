---
title: MPI_File_read function
TOCTitle: MPI_File_read function
ms:assetid: 442a3d4f-5344-4ef1-bdec-b6a08f866c19
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473340(v=VS.85)
ms:contentKeyID: 59360876
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_READ
- mpif/MPI_File_read
- mpi/MPI_FILE_READ
dev_langs:
- C++
- C
description: Master the MPI_File_read function with Microsoft's comprehensive guide. Learn syntax, parameters, return values, and more. Perfect for HPC Pack users.
---

# MPI\_File\_read function

Read using individual file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_read(
        MPI_File     file,
  _Out_ void         *buf,
        int          count,
        MPI_Datatype datatype,
  _Out_ MPI_Status   *status
);
```

## Parameters

  - *file*  
    File handle.

  - *buf* \[out\]  
    Initial address of buffer.

  - *count*  
    Number of elements in buffer.

  - *datatype*  
    Datatype of each buffer element.

  - *status* \[out\]  
    Status object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_READ(FH, BUF, COUNT, DATATYPE, STATUS, IERROR)
        <type> BUF(*)
        INTEGER FH, COUNT, DATATYPE, STATUS(MPI_STATUS_SIZE), IERROR
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

[MPI File Functions](mpi-file-functions.md)

