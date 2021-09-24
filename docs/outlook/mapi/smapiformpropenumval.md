---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ea204f2f1cf324b4276563005c2cd90ac53e0c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549911"
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

## <a name="members"></a>メンバー

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

