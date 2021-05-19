---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435412"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
マップの表示名に列挙された整数値を指定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszDisplayName**
  
> **nVal** メンバーで指定された値の表示名を含む文字列。 
    
 **nVal**
  
> **pszDisplayName** メンバーが指す表示名の列挙値。 
    
## <a name="remarks"></a>注釈

ユーザーがフォームから表示名を選択すると、フォームに関連付けられた [IMAPIProp](imapipropiunknown.md) インターフェイス実装を使用して、名前の対応する列挙値が格納されます。 
  
## <a name="see-also"></a>関連項目



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

