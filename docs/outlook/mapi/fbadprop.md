---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800027"
---
# <a name="fbadprop"></a>FBadProp

  
  
**適用対象**: Outlook 
  
指定されたプロパティを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>パラメーター

 _lpprop_
  
> [in]検証するプロパティを定義する[SPropValue](spropvalue.md)構造体です。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定されたプロパティが有効ではありません。 
    
FALSE 
  
> 指定したプロパティは、無効です。
    
## <a name="remarks"></a>注釈

サービス プロバイダーは、プロパティを設定する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドへの呼び出しの準備など、いくつかの理由の**FBadProp**関数を呼び出すことができます。 **FBadProp**は、プロパティの型によって指定されたプロパティを検証します。 たとえば、プロパティがブール値の場合は、 **FBadProp** sures の値が TRUE または false を指定します。 プロパティがバイナリの場合は、 **FBadProp**のポインターとサイズを確認、正しく割り当てられていることを確認します。 
  
## <a name="see-also"></a>関連項目



[FBadPropTag](fbadproptag.md)

