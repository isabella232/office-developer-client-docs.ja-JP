---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414614"
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
  

