---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b2caa70600bd32234e38420f274bcd5c46ffb070
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578158"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ クラスの文字列へのポインターの配列が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|関連するマクロ:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Members

 **あう**
  
> 配列内のメッセージ クラスの文字列ポインターの数。
    
 **aMessageClass**
  
> メッセージ クラスの文字列へのポインターの配列です。
    
## <a name="remarks"></a>注釈

**SMessageClassArray**構造体は、次のメソッドのパラメーターとして渡されます。 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

