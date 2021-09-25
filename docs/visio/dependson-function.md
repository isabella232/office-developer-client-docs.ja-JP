---
title: DEPENDSON 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
ms.localizationpriority: medium
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: セル参照の依存関係を作成します。
ms.openlocfilehash: f97ba98cbc5e2a56578b5303583a1d2811242f67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608236"
---
# <a name="dependson-function"></a>DEPENDSON 関数

セル参照の依存関係を作成します。
  
## <a name="syntax"></a>構文

DEPENDSON(** *cellref* ** [, ** *cellref2 **,...])* 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |必須  <br/> |**String** <br/> |最初のセル参照を指定します。  <br/> |
| _cellref2_ <br/> |省略可能  <br/> |**String** <br/> |2 番目のセル参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この関数は常に FALSE を返します。[Event] 行または [Action] セルで使用した場合には効果がありません。 
  
## <a name="example"></a>例

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
図形の [PinX] または [PinY] セルが変更された場合に必ず、図形のテキスト ブロックを開きます。 
  

