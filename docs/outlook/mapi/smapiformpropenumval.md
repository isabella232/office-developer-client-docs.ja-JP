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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578718"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
列挙された整数値をその値の表示名にマップします。 
  
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
  
> **NVal**のメンバーで指定された値の表示名を含む文字列です。 
    
 **nVal**
  
> **PszDisplayName**メンバーで指定された表示名の列挙値。 
    
## <a name="remarks"></a>注釈

ユーザーは、フォームの表示名を選択すると、フォームに関連付けられている[IMAPIProp](imapipropiunknown.md)インターフェイスの実装を使用して名前の対応する列挙値が格納されます。 
  
## <a name="see-also"></a>関連項目



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

