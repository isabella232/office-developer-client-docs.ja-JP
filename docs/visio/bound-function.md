---
title: BOUND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
ms.localizationpriority: medium
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: 1 つの範囲または複数の範囲にセルの値を制約します。
ms.openlocfilehash: 0190ae3b3066ffc15232574c83719b732bedc2a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613115"
---
# <a name="bound-function"></a>BOUND 関数

1 つの範囲または複数の範囲にセルの値を制約します。
  
## <a name="syntax"></a>構文

BOUND (** *value* **, ** *type* **, ** ignore **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** )  
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |制約される現在の値を指定します。  <br/> |
| _type_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |制約が包括的 (0) であるか、排他的 (1) であるか、または無効 (2) であるかを指定します。  <br/> |
| _ignore_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> | 範囲を無視する場合は TRUE。セルの値を範囲に制限するには、FALSE を指定します。  <br/> |
| _value1_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |範囲内の最初の値を指定します。  <br/> |
| _value2_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |範囲内の 2 番目の値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

たとえば、セルの値を上限と下限に制限するには、BOUND 関数を使用して、最小または最大の高さの上下に伸ばさないオブジェクトを制御します。 この制約は、範囲または範囲に関して包括的または排他的に指定できます。 現在の値を制限しない場合は  _、type_ パラメーターを 2 (無効) に設定します。 
  
複数の範囲を定義するには、ignore パラメーター _、value1 パラメーター、value2_ パラメーターを複数 _指定_ します。  ignore パラメーター  _を使用_ して、特定の範囲の制約を無効にします。 
  
BOUND 関数を含む数式は、値が変更しても上書きされません。代わりに、数式が保持され、新しい値が value パラメーターに  _配置_ されます。 
  
## <a name="example-1"></a>例 1

この例では、BOUND 関数を使用して、コントロール ハンドルを図形の境界ボックス内に保持します。 
  
Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)
  
Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)
  
## <a name="example-2"></a>例 2

この例では、BOUND 関数を使用して、図形の幅を 2 インチ、4 インチ、または 6 インチ に制約します。 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

