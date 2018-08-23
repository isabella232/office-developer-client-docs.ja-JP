---
title: UPPER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: 大文字に変換された文字列を返します。
ms.openlocfilehash: df8250ef634b04cb19cbb4e120bd02eb77531a82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806728"
---
# <a name="upper-function"></a>UPPER 関数

大文字に変換された文字列を返します。
  
## <a name="syntax"></a>構文

上 (* **式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**可変型 (Varies)** <br/> | 文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、大文字に変換されます。  <br/> |
   
## <a name="remarks"></a>注釈

大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。 
  
## <a name="example"></a>例

UPPER("mIxEd CAse") 
  
"MIXED CASE" を返します。 
  

