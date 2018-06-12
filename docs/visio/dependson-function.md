---
title: DEPENDSON 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: セル参照の依存関係を作成します。
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805212"
---
# <a name="dependson-function"></a>DEPENDSON 関数

セル参照の依存関係を作成します。
  
## <a name="syntax"></a>構文

DEPENDSON (* * *cellref* * * [、* * *cellref2* * *,...]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |最初のセル参照を指定します。  <br/> |
| _cellref2_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |2 番目のセル参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この関数は常に FALSE を返します。[Event] 行または [Action] セルで使用した場合には効果がありません。 
  
## <a name="example"></a>例

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
図形の [PinX] または [PinY] セルが変更された場合に必ず、図形のテキスト ブロックを開きます。 
  

