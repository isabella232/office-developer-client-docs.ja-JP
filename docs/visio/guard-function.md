---
title: GUARD 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: 実行されるアクション、図面ウィンドウ、たとえば、移動、サイズ変更、グループ化、または図形のグループ化を解除して、削除、および変更から式を保護します。
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805493"
---
# <a name="guard-function"></a>GUARD 関数

実行されるアクション、図面ウィンドウ、たとえば、移動、サイズ変更、グループ化、または図形のグループ化を解除して、削除、および変更から*式*を保護します。 
  
## <a name="syntax"></a>構文

ガード (* **式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。  <br/> |
   
## <a name="remarks"></a>注釈

GUARD 関数による影響を受ける主なセルは、[Width]、[Height]、[PinX]、[PinY] です。 
  
セルの数式を保護すると、図面ウィンドウでのアクションによってそのセルの値が変更されるのを防ぐことができます。ただし、図面ウィンドウで行う 1 つのアクションが複数のセルに影響することがあるため、図形の外観に予期しない変更が生じないようにするには、個々のセルを保護する必要があります。 
  
## <a name="example"></a>例

GUARD(TEXTWIDTH(TheText) + 0.5 in) 
  
図形の [Shape Transform] セクションの [Width] セルにこの式を設定すると、図面ウィンドウの図形の幅が変更されたときに式 (TEXTWIDTH(TheText) + 0.5 in) が別の値に置き換えられるのを防ぐことができます。TheText には関連する図形のテキストの構成が変更されたときにトリガーされるセルを指定します。 
  

