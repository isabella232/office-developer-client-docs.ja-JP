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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433648"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したプロパティ タグを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> [in]検証するプロパティ タグ。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定したプロパティ タグが有効な MAPI プロパティ タグではありません。 
    
FALSE 
  
> 指定したプロパティ タグは、有効な MAPI プロパティ タグです。
    
## <a name="remarks"></a>注釈

**FBadPropTag** 関数は、MAPI 定義に基づいて指定されたプロパティ タグを検証します。 プロパティの種類が MAPI で定義された型の 1 つであり、プロパティ識別子がその型として定義されている必要があります。 
  
## <a name="see-also"></a>関連項目



[FBadProp](fbadprop.md)

