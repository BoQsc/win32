---
title: IVMTask IsCancelable property (VPCCOMInterfaces.h)
description: Determines whether the task can be canceled.
ms.assetid: abb8a29a-7f5b-45ba-ae79-d422dfb2f39d
keywords:
- IsCancelable property Virtual PC
- IsCancelable property Virtual PC , IVMTask interface
- IVMTask interface Virtual PC , IsCancelable property
topic_type:
- apiref
api_name:
- IVMTask.IsCancelable
- IVMTask.get_IsCancelable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
---

# IVMTask::IsCancelable property

\[Windows Virtual PC is no longer available for use as of Windows 8. Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determines whether the task can be canceled.

This property is read-only.

## Syntax


```C++
HRESULT get_IsCancelable(
  [out, retval] VARIANT_BOOL *isCancelable
);
```



## Property value

**TRUE** if the task can be canceled before completion and **FALSE** otherwise.

## Error codes



| Name/value                                                                                                                                                    | Meaning                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S\_OK</dt> <dt>0</dt> </dl>                       | The operation was successful.<br/>     |
| <dl> <dt>E\_POINTER</dt> <dt>0x80004003</dt> </dl>         | The parameter value is **NULL**.<br/>  |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt> </dl> | An unexpected error has occurred.<br/> |



## Requirements



|                                     |                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                                    |
| Minimum supported server<br/> | None supported<br/>                                                                     |
| End of client support<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## See also

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

