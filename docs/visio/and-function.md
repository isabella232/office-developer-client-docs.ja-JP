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
description: TRUE をすべての論理式を指定する場合は、TRUE (1) を返します。 FALSE または 0 の論理式のいずれかの場合は、AND 関数は FALSE (0) を返します。
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804786"
---
# <a name="and-function"></a>AND 関数

TRUE をすべての論理式を指定する場合は、TRUE (1) を返します。 FALSE または 0 の論理式のいずれかの場合は、AND 関数は FALSE (0) を返します。
  
## <a name="syntax"></a>構文

(* **論理 expression1* * *、* **論理式 2* * *,...、* **論理 expressionN* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _論理式_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。ゼロ以外の値に評価される式はすべて TRUE であると見なされます。  <br/> |
   
## <a name="example"></a>例

(高さ\>1 の場合、[pinx] \> 1)
  
両方の式が TRUE の場合、TRUE を返します。いずれかの式が FALSE の場合、FALSE を返します。
  

