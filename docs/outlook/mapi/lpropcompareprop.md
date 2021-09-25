---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b08be76fa214570dcc336431fe227a8629762de6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584186"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つのプロパティ値を比較して、等しいかどうかを判断します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValueA_
  
> [in]比較する最初 [のプロパティ値](spropvalue.md) を定義する SPropValue 構造体へのポインター。 
    
 _lpSPropValueB_
  
> [in]比較する **2 番目の** プロパティ値を定義する SPropValue 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

 **LPropCompareProp** は、ほとんどのプロパティ型に対して次のいずれかの値を返します。 
  
- _lpSPropValueA_ パラメーターで示される値が _lpSPropValueB_ パラメーターで示される値より小さい場合は、0 未満です。 
    
- _lpSPropValueA_ で示される値が _lpSPropValueB_ で示される値より大きい場合は、0 より大きい。
    
- _lpSPropValueA_ で示される値が _lpSPropValueB_ で示される値と等しい場合は 0 です。 
    
ブール型やエラー型など、組み込みの順序付けがないプロパティ型の場合、2 つのプロパティ値が等しくない場合 **、LPropCompareProp** 関数は未定義の値を返します。 この未定義の値は 0 以外で、呼び出し間で一貫性があります。 
  
## <a name="remarks"></a>注釈

**LPropCompareProp** 関数は、比較する 2 つのプロパティの種類が同じ場合にのみ使用します。 
  
**LPropCompareProp** を呼び出す前に、クライアント アプリケーションまたはサービス プロバイダーは、[まず IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しとの比較のためにプロパティを取得する必要があります。 クライアントまたはプロバイダーが **LPropCompareProp** を呼び出す場合、関数は最初にプロパティ タグを調べて、プロパティ値の比較が有効か確認します。 次に、関数はプロパティ値を比較し、適切な値を返します。 
  
プロパティの値が等しくない場合 **、LPropCompareProp は** 、どちらが大きいのか判断します。 **LPropCompareProp が** 比較するプロパティは、同じオブジェクトに属している必要があります。 
  

