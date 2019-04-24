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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309493"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
列挙された整数値をその値の表示名にマップします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszdisplayname**
  
> **nval**メンバーで指定された値の表示名を含む文字列。 
    
 **nval**
  
> **pszdisplayname**メンバーによって示される表示名の列挙値。 
    
## <a name="remarks"></a>解説

ユーザーがフォームから表示名を選択すると、その名前の対応する列挙値は、フォームに関連付けられている[imapiprop](imapipropiunknown.md)インターフェイスの実装を使用して格納されます。 
  
## <a name="see-also"></a>関連項目



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

