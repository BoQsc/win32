---
Description: Draw several instances of the same subset of a mesh.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::DrawSubsetInstanced method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DX10Mesh::DrawSubsetInstanced method

Draw several instances of the same subset of a mesh.

## Syntax


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## Parameters

<dl> <dt>

*AttribId* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Specifies which subset of the mesh to draw. This value is used to differentiate faces in a mesh as belonging to one or more attribute groups. See remarks.

</dd> <dt>

*InstanceCount* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Number of instances to render.

</dd> <dt>

*StartInstanceLocation* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Which instance to start fetching from in each buffer marked as instance data.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).

## Remarks

A mesh contains an attribute table. The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID. For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:



|            |                 |
|------------|-----------------|
| AttribID 0 | Faces 0 ~ 50    |
| AttribID 1 | Faces 51 ~ 125  |
| AttribID 2 | Faces 126 ~ 200 |



 

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be to draw the same object with different positions and colors. Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.

Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/windows/desktop/c3d54072-1deb-324f-2e02-e048a4a438a0). The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.

The following code illustrates extracting the vertex and index buffers from the mesh object.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &amp;vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&amp;indexBuffer);
      
```



## Requirements



|                    |                                                                                       |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Library<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## See also

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 



