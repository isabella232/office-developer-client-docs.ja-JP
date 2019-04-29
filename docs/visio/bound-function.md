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
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425961"
---
# <a name="bound-function"></a>BOUND 関数

1 つの範囲または複数の範囲にセルの値を制約します。
  
## <a name="syntax"></a>構文

BOUND (* **値** *、* * *type* * *、* * *ignore* * *、* * *value1* * *、* * *value2* * * * * * [, ignore (n)、value1 (n)、value2 (n),...] * * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |必須  <br/> |**数値** <br/> |制約される現在の値を指定します。  <br/> |
| _type_ <br/> |必須  <br/> |**数値** <br/> |制約が包括的 (0) であるか、排他的 (1) であるか、または無効 (2) であるかを指定します。  <br/> |
| _フォント_ <br/> |必須  <br/> |**Boolean** <br/> | TRUE を指定すると、範囲は無視されます。FALSE を指定すると、セルの値が範囲に制限されます。  <br/> |
| _value1_ <br/> |必須  <br/> |**数値** <br/> |範囲内の最初の値を指定します。  <br/> |
| _value2_ <br/> |必須  <br/> |**数値** <br/> |範囲内の 2 番目の値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

bound 関数を使用して、セルの値を上限と下限に制限します。たとえば、最小または最大の高さより上または下に拡大してはならないオブジェクトを制御します。 範囲または範囲を基準として、制約を包含または排他的にすることができます。 現在の値を制約しないようにするには、 _type_パラメーターを 2 (無効) に設定します。 
  
複数の範囲を定義するには、 _ignore_、 _value1_、および_value2_の各パラメーターを複数回指定します。 特定の範囲によって制約を無効にするには、 _ignore_パラメーターを使用します。 
  
BOUND 関数を含む数式は、その値が変更されても上書きされません。代わりに、数式は保持され、新しい値は_value_パラメーターに配置されます。 
  
## <a name="example-1"></a>例 1

この例では、BOUND 関数を使用して、コントロール ハンドルを図形の境界ボックス内に保持します。 
  
コントロール X1 = BOUND (幅\*0.5、0、FALSE、幅\*0、幅\*1)
  
コントロール. Y1 = BOUND (高さ\*0.5、0、FALSE、高さ\*0、高さ\*1)
  
## <a name="example-2"></a>例 2

この例では、BOUND 関数を使用して、図形の幅を 2 インチ、4 インチ、または 6 インチ に制約します。 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

