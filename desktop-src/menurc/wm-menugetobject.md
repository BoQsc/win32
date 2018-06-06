---
title: WM\_MENUGETOBJECT message
description: Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT message Menus and Other Resources
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WM\_MENUGETOBJECT message

Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.


```C++
#define WM_MENUGETOBJECT                0x0124
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

This parameter is not used.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**MENUGETOBJECTINFO**](/windows/desktop/api/Winuser/ns-winuser-tagmenugetobjectinfo) structure.

</dd> </dl>

## Return value

The application should return one of the following values.



| Return code/value                                                                                                                                                | Description                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt> </dl>     | An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/desktop/api/Winuser/ns-winuser-tagmenugetobjectinfo)<br/> |
| <dl> <dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt> </dl> | The interface is not supported.<br/>                                                                             |



 

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[Menus Overview](menus.md)
</dt> </dl>

 

 




