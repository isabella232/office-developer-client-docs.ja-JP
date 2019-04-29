---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427158"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した関係演算子を使用して、2つのプロパティの値を比較します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>パラメーター

_lpSPropValue1_
  
> 順番比較のための最初のプロパティ値を定義する[spropvalue](spropvalue.md)構造体へのポインター。 
    
_ulrelop_
  
> 順番比較で使用する関係演算子を示します。 許容値については、 [scomparepropsrestriction](scomparepropsrestriction.md)構造を参照してください。 
    
_lpSPropValue2_
  
> 順番比較の2番目のプロパティの値を定義する**spropvalue**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> プロパティ値は、指定されたリレーションを満たします。 
    
FALSE 
  
> プロパティの値は、指定されたリレーションシップを満たしていません。
    
## <a name="remarks"></a>注釈

比較方法は、 [spropvalue](spropvalue.md)プロパティの定義で指定されているプロパティの種類によって異なります。 **fpropcompareprop**および[fpropの prop](fpropcontainsprop.md)関数を使用して、テーブルの生成に関する制限を準備できます。 
  
比較の順序は_lpSPropValue1_、_ ulrelop _、_ lpSPropValue2 _ です。 比較するプロパティ値のプロパティの種類が一致しない場合、 **fpropcompareprop**関数は FALSE を返します。 
  

