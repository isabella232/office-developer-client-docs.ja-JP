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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412696"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージクラスの文字列へのポインターの配列を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|関連するマクロ:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>メンバー

 **cvalues**
  
> 配列内のメッセージクラス文字列ポインターの数。
    
 **amessageclass**
  
> メッセージクラスの文字列へのポインターの配列です。
    
## <a name="remarks"></a>注釈

**SMessageClassArray**構造体は、次のメソッドのパラメーターとして渡されます。 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

