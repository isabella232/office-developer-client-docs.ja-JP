---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eeeaff3a4cd3097511c50f8761880c270650eb39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629572"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ クラス文字列へのポインターの配列を格納します。
  
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

## <a name="members"></a>メンバー

 **cValues**
  
> 配列内のメッセージ クラス文字列ポインターの数。
    
 **aMessageClass**
  
> メッセージ クラス文字列へのポインターの配列。
    
## <a name="remarks"></a>注釈

**SMessageClassArray** 構造体は、次のメソッドでパラメーターとして渡されます。 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

