---
title: LOWER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: 小文字に変換された文字列を返します。
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805808"
---
# <a name="lower-function"></a>LOWER 関数

小文字に変換された文字列を返します。
  
## <a name="syntax"></a>構文

下 (* **式** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**によって異なります** <br/> | 文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、小文字に変換されます。  <br/> |
   
### <a name="return-value"></a>�߂�l

文字列
  
## <a name="remarks"></a>注釈

大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。 
  
## <a name="example"></a>例

LOWER("mIxEd CAse") 
  
"mixed case" を返します。 
  

