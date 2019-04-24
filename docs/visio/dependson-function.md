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
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360235"
---
# <a name="dependson-function"></a>DEPENDSON 関数

セル参照の依存関係を作成します。
  
## <a name="syntax"></a>構文

DEPENDSON (* * *cellref* * * [, * * *cellref2* * *,...]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |必須  <br/> |**String** <br/> |最初のセル参照を指定します。  <br/> |
| _cellref2_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |2 番目のセル参照を指定します。  <br/> |
   
## <a name="remarks"></a>解説

この関数は常に FALSE を返します。[Event] 行または [Action] セルで使用した場合には効果がありません。 
  
## <a name="example"></a>例

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
図形の [PinX] または [PinY] セルが変更された場合に必ず、図形のテキスト ブロックを開きます。 
  

