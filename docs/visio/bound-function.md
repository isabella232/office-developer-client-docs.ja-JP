---
title: BOUND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: 1 つの範囲または複数の範囲にセルの値を制約します。
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804949"
---
# <a name="bound-function"></a>BOUND 関数

1 つの範囲または複数の範囲にセルの値を制約します。
  
## <a name="syntax"></a>構文

バインド (* **値** *、* **型** *、* **無視** *、* * *value1* * *、* **値 2* * * * * * [、ignore(n)、value1(n)、value2(n)、...] * * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |制約される現在の値を指定します。  <br/> |
| _type_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |制約が包括的 (0) であるか、排他的 (1) であるか、または無効 (2) であるかを指定します。
  <br/> |
| _無視します。_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> | 範囲を無視する場合は TRUE。範囲にセルの値を制約する場合は FALSE です。  <br/> |
| _値 1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |範囲内の最初の値を指定します。
  <br/> |
| _値 2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |範囲内の 2 番目の値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

BOUND 関数を使用すると、セルの値を上限と下限値、たとえば、最小または最大の高さより上または下にない拡大するかのオブジェクトを制御するために制限できます。 制約は、包括的または排他的な範囲にあります。 現在の値を制限しない必要がある場合、2 の (無効) に_型_パラメーターを設定します。 
  
_無視_、 _value1_と_value2_のパラメーターの複数のオカレンスを指定することによって、複数の範囲を定義できます。 _無視する_パラメーターを使用して、特定の範囲による制約を無効にします。 
  
BOUND 関数を含む数式がその値が変更されると上書きされません。代わりに、数式は保持し、新しい値が_value_パラメーターに配置されます。 
  
## <a name="example-1"></a>例 1

この例では、BOUND 関数を使用して、コントロール ハンドルを図形の境界ボックス内に保持します。 
  
Controls.X1 = バインド (幅\*0.5、0、FALSE、幅\*0、幅\*1)
  
Controls.Y1 = バインド (高さ\*0.5、0、FALSE、高さ\*0、高さ\*1)
  
## <a name="example-2"></a>例 2

この例では、BOUND 関数を使用して、図形の幅を 2 インチ、4 インチ、または 6 インチ に制約します。 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

