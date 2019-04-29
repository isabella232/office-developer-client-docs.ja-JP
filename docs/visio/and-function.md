---
title: AND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: 指定されたすべての論理式が true の場合は、true (1) を返します。 論理式のいずれかが false または0の場合、AND 関数は false (0) を返します。
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422013"
---
# <a name="and-function"></a>AND 関数

指定されたすべての論理式が true の場合は、true (1) を返します。 論理式のいずれかが false または0の場合、AND 関数は false (0) を返します。
  
## <a name="syntax"></a>構文

AND (* * *logical expression1* * *、* **論理 expression2* * *,..., * **論理式 n* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _論理式_ <br/> |必須  <br/> |**String** <br/> | 定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。ゼロ以外の値に評価される式はすべて TRUE であると見なされます。  <br/> |
   
## <a name="example"></a>例

AND (Height \> 1, PinX \> 1)
  
両方の式が TRUE の場合、TRUE を返します。 いずれかの式が FALSE の場合、FALSE を返します。
  

