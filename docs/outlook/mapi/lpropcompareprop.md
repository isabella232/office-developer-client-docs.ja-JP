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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801299"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**適用対象**: Outlook 
  
等しいかどうかを確認するのには 2 つのプロパティの値を比較します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValueA_
  
> [in][SPropValue](spropvalue.md)構造体を比較する最初のプロパティの値を定義することへのポインター。 
    
 _lpSPropValueB_
  
> [in]**SPropValue**構造体を比較する 2 番目のプロパティの値を定義することへのポインター。 
    
## <a name="return-value"></a>戻り値

 **LPropCompareProp**では、ほとんどのプロパティの種類を次の値のいずれかを返します。 
  
- 0 より小さいによって値が指定されている場合、 _lpSPropValueA_パラメーターは、 _lpSPropValueB_パラメーターで指定されたよりも短い。 
    
- _LpSPropValueB_によって示されるよりも大きく、値が_lpSPropValueA_で示されている場合は 0 より大きい値です。
    
- 値が_lpSPropValueA_で示されている場合は 0 では、 _lpSPropValueB_によって示される値と等しい。 
    
ブール値など、組み込みの順序がないプロパティの種類またはエラーの種類は、 **LPropCompareProp**関数は、2 つのプロパティの値が等しくない場合に未定義の値を返します。 この未定義の値は 0 以外の値と一貫性のある複数の呼び出し 
  
## <a name="remarks"></a>注釈

のみを比較する 2 つのプロパティの型が同じ場合は、 **LPropCompareProp**関数を使用します。 
  
**LPropCompareProp**を呼び出す前にクライアント アプリケーションまたはサービス プロバイダーする必要があります最初にプロパティを取得、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しと比較するため。 クライアントまたはプロバイダーの呼び出し**LPropCompareProp**関数が最初にいることを確認するのにはプロパティ タグを確認すると、プロパティ値の比較は、有効です。 関数は、適切な値を返すプロパティの値を比較します。 
  
プロパティの値が等しくない場合は、 **LPropCompareProp**は、どちらが大きい方を決定します。 **LPropCompareProp**を比較するプロパティは、同じオブジェクトに属している必要はありません。 
  

