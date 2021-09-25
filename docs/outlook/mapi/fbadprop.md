---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2274fa324425bfc3e04ec5a6a45ff1270cbfbca8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621151"
---
# <a name="fbadprop"></a>FBadProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定済みのプロパティを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>パラメーター

 _lpprop_
  
> [in] 検証されるプロパティを定義する [SPropValue](spropvalue.md) 構造です。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定済みのプロパティが無効です。 
    
FALSE 
  
> 指定済みのプロパティは有効です。
    
## <a name="remarks"></a>備考

サービス プロバイダーは **FBadProp** 関数を呼び出すことができます。プロパティを設定する [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備など、さまざまな用途に使用することができます。 **FBadProp** はプロパティの種類に応じて、指定済みのプロパティを検証します。 たとえば、プロパティがブール値の場合、**FBadProp** は、その値が TRUE または FALSE のいずれかであることを確認します。 プロパティがバイナリの場合は、**FBadProp** は、そのポインターおよびサイズのチェックを行い、正しく割り当てられていることを確認します。 
  
## <a name="see-also"></a>関連項目



[FBadPropTag](fbadproptag.md)

