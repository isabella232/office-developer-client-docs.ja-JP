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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564606"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**適用されます**: Outlook 2013 |Outlook 2016 
  
指定したリレーショナル演算子を使用して 2 つのプロパティ値を比較します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>パラメーター

_lpSPropValue1_
  
> [in]比較のための最初のプロパティ値を定義する[SPropValue](spropvalue.md)構造体へのポインター。 
    
_ulRelOp_
  
> [in]比較で使用する関係演算子です。 許容値は、 [SComparePropsRestriction](scomparepropsrestriction.md)構造体を参照してください。 
    
_lpSPropValue2_
  
> [in]**SPropValue**構造体の比較の 2 番目のプロパティの値を定義することへのポインター。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> プロパティの値は、指定された関係を満たします。 
    
FALSE 
  
> プロパティの値は、指定したリレーションシップを満たしていません。
    
## <a name="remarks"></a>注釈

比較メソッドは、 [SPropValue](spropvalue.md)プロパティの定義で指定されたプロパティの型によって異なります。 テーブルを生成するための制限を準備するのには、 **FPropCompareProp**と[FPropContainsProp](fpropcontainsprop.md)関数を使用できます。 
  
比較の順序は、 _lpSPropValue1_、_ ulRelOp _ _ lpSPropValue2 _ です。 比較するプロパティの値のプロパティの型が一致しない場合、 **FPropCompareProp**関数は FALSE を返します。 
  

