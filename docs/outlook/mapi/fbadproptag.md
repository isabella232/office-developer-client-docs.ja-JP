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
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341000"
---
# <a name="fbadproptag"></a>FBadPropTag

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定されたプロパティタグを検証します。 
  
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
  
> 順番検証するプロパティタグ。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定されたプロパティタグは、有効な MAPI プロパティタグではありません。 
    
FALSE 
  
> 指定されたプロパティタグは、有効な MAPI プロパティタグです。
    
## <a name="remarks"></a>解説

**FBadPropTag**関数は、MAPI 定義に基づいて指定されたプロパティタグを検証します。 プロパティの型が MAPI で定義されている型の1つであり、プロパティ識別子がその型に定義されていることを sures にします。 
  
## <a name="see-also"></a>関連項目



[FBadProp](fbadprop.md)

