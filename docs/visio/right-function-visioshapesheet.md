---
title: RIGHT 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: 指定した文字数に基づいて、文字列の最後の文字または文字列を返します。
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806232"
---
# <a name="right-function-visioshapesheet"></a>RIGHT 関数 (VisioShapeSheet)

指定した文字数に基づいて、文字列の最後の文字または文字列を返します。
  
## <a name="syntax"></a>構文

右 (* **テキスト** * [、* * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 抽出する文字を含む文字列を指定します。  <br/> |
| _num_chars_opt_ <br/> |省略可能  <br/> |**番号** <br/> |抽出する文字数を指定します。既定値は 1 です。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

_Num_chars_opt_の値は、以上のゼロ (0) にする必要があります。 
  
_Num_chars_opt_が文字列の長さよりも大きい場合は、右はすべてのテキストを返します。 _Num_chars_opt_が省略された場合は 1 であると見なされます。 
  
## <a name="example"></a>例

RIGHT ("January 1, 2004", 4) 
  
値 2004 を返します。 
  

