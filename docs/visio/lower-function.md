---
title: LOWER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
ms.localizationpriority: medium
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: 小文字に変換された文字列を返します。
ms.openlocfilehash: 4021eb5952a3718e74e8e1c16f72268d08ae3832
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615859"
---
# <a name="lower-function"></a>LOWER 関数

小文字に変換された文字列を返します。
  
## <a name="syntax"></a>構文

LOWER(** *expression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> | 文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、小文字に変換されます。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。 
  
## <a name="example"></a>例

LOWER("mIxEd CAse") 
  
"mixed case" を返します。 
  

