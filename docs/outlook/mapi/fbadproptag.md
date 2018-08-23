---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800039"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**適用対象**: Outlook 
  
指定されたプロパティ タグを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> [in]検証するプロパティ タグです。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定されたプロパティ タグは、有効な MAPI プロパティ タグではありません。 
    
FALSE 
  
> 指定されたプロパティ タグは、有効な MAPI プロパティ タグです。
    
## <a name="remarks"></a>注釈

**FBadPropTag**関数では、MAPI 定義に基づいて、指定されたプロパティ タグを検証します。 Sures プロパティの型は、MAPI によって定義された型のいずれかをその型のプロパティの識別子が定義されていることを確認します。 
  
## <a name="see-also"></a>関連項目



[FBadProp](fbadprop.md)

