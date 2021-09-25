---
title: GUARD 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
ms.localizationpriority: medium
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: 図形の移動、サイズ変更、グループ化、グループ化解除など、図面ウィンドウで実行されるアクションによって、削除や変更から式を保護します。
ms.openlocfilehash: 07398bc6360b231ce7a9b8bd6f64635db03d57ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554685"
---
# <a name="guard-function"></a>GUARD 関数

図形の  *移動*  、サイズ変更、グループ化、グループ化解除など、図面ウィンドウで実行されるアクションによって、削除や変更から式を保護します。 
  
## <a name="syntax"></a>構文

GUARD(** *式* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。  <br/> |
   
## <a name="remarks"></a>注釈

GUARD 関数による影響を受ける主なセルは、[Width]、[Height]、[PinX]、[PinY] です。 
  
セルの数式を保護すると、図面ウィンドウでのアクションによってそのセルの値が変更されるのを防ぐことができます。ただし、図面ウィンドウで行う 1 つのアクションが複数のセルに影響することがあるため、図形の外観に予期しない変更が生じないようにするには、個々のセルを保護する必要があります。 
  
## <a name="example"></a>例

GUARD(TEXTWIDTH(TheText) + 0.5 in) 
  
図形の [Shape Transform] セクションの [Width] セルにこの式を設定すると、図面ウィンドウの図形の幅が変更されたときに式 (TEXTWIDTH(TheText) + 0.5 in) が別の値に置き換えられるのを防ぐことができます。TheText には関連する図形のテキストの構成が変更されたときにトリガーされるセルを指定します。 
  

