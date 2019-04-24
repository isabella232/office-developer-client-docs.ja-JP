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
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357436"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つのプロパティ値が等しいかどうかを比較します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>パラメーター

 _lpspropvaluea_
  
> 順番比較する最初のプロパティ値を定義する[spropvalue](spropvalue.md)構造体へのポインター。 
    
 _lpspropvalueb_
  
> 順番比較する2番目のプロパティ値を定義する**spropvalue**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

 **lpropcompareprop**は、ほとんどのプロパティの種類について、次のいずれかの値を返します。 
  
- _lpspropvaluea_パラメーターによって指定された値が_lpspropvaluea_パラメーターによって示される値よりも小さい場合は、0未満です。 
    
- _lpspropvaluea_で指定された値が_lpspropvaluea_で示される値よりも大きい場合は、0より大きい値を指定します。
    
- _lpspropvaluea_で指定された値が_lpspropvaluea_によって示される値と等しい場合は0。 
    
ブール型 (Boolean) やエラーの種類など、組み込みの順序付けを持たないプロパティの種類の場合、 **lpropcompareprop**関数は、2つのプロパティの値が等しくない場合に未定義の値を返します。 この未定義の値は、0以外の呼び出しで一貫しています。 
  
## <a name="remarks"></a>解説

2つのプロパティの比較対象の型が同じ場合にのみ、 **lpropcompareprop**関数を使用してください。 
  
**lpropcompareprop**を呼び出す前に、クライアントアプリケーションまたはサービスプロバイダーは、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドの呼び出しと比較するプロパティを最初に取得する必要があります。 クライアントまたはプロバイダーが**lpropcompareprop**を呼び出すと、まず、プロパティの値の比較が有効であることを確認するために、最初にプロパティタグを調べます。 次に、プロパティの値を比較し、適切な値を返します。 
  
プロパティの値が等しくない場合は、 **lpropcompareprop**によって、どちらが大きくなるかが決まります。 **lpropcompareprop**と比較するプロパティは、同じオブジェクトに属している必要はありません。 
  

