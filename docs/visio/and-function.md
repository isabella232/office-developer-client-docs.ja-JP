---
title: AND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
ms.localizationpriority: medium
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: 指定された論理式のすべてが TRUE の場合は、TRUE (1) を返します。 論理式が FALSE または 0 の場合、AND 関数は FALSE (0) を返します。
ms.openlocfilehash: 82ce384641c400764356d3288ae7d903ee901292
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628879"
---
# <a name="and-function"></a>AND 関数

指定された論理式のすべてが TRUE の場合は、TRUE (1) を返します。 論理式が FALSE または 0 の場合、AND 関数は FALSE (0) を返します。
  
## <a name="syntax"></a>構文

AND(** *論理式1* **, ** *論理式2* **,..., ** *論理式 *** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _論理式_ <br/> |必須  <br/> |**String** <br/> | 定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。ゼロ以外の値に評価される式はすべて TRUE であると見なされます。  <br/> |
   
## <a name="example"></a>例

AND(Height \> 1, PinX \> 1)
  
両方の式が TRUE の場合、TRUE を返します。いずれかの式が FALSE の場合、FALSE を返します。
  

