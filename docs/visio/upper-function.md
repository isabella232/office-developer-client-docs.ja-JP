---
title: UPPER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
ms.localizationpriority: medium
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: 大文字に変換された文字列を返します。
ms.openlocfilehash: aad79f5b04f94bcfe12615d6e0498fbf501f0e49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622670"
---
# <a name="upper-function"></a>UPPER 関数

大文字に変換された文字列を返します。
  
## <a name="syntax"></a>構文

UPPER(** *expression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> | 文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、大文字に変換されます。  <br/> |
   
## <a name="remarks"></a>注釈

大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。 
  
## <a name="example"></a>例

UPPER("mIxEd CAse") 
  
"MIXED CASE" を返します。 
  

