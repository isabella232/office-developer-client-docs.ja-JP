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
  
指定した関係演算子を使用して 2 つのプロパティ値を比較します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>パラメーター

_lpSPropValue1_
  
> [in]比較の最初 [のプロパティ値](spropvalue.md) を定義する SPropValue 構造体へのポインター。 
    
_ulRelOp_
  
> [in]比較で使用する関係演算子。 許容値については [、「SComparePropsRestriction 構造体」を参照](scomparepropsrestriction.md) してください。 
    
_lpSPropValue2_
  
> [in]比較用の **2 番目の** プロパティ値を定義する SPropValue 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> プロパティの値は、指定された関係を満たします。 
    
FALSE 
  
> プロパティの値は、指定された関係を満たさない。
    
## <a name="remarks"></a>注釈

比較メソッドは [、SPropValue](spropvalue.md) プロパティ定義で指定されたプロパティの種類によって異なります。 **FPropCompareProp** 関数と [FPropContainsProp](fpropcontainsprop.md)関数を使用して、テーブルを生成するための制限を準備できます。 
  
比較の順序は  _lpSPropValue1_、 _ ulRelOp _, _ lpSPropValue2 _です。 比較するプロパティ値のプロパティの種類が一致しない場合 **、FPropCompareProp** 関数は FALSE を返します。 
  

