---
title: LEFT 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: 指定した文字数に基づいて、文字列の左端の文字または文字列を返します。
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805686"
---
# <a name="left-function-visioshapesheet"></a>LEFT 関数 (VisioShapeSheet)

指定した文字数に基づいて、文字列の左端の文字または文字列を返します。
  
## <a name="syntax"></a>構文

左 (* **テキスト** *、[、* * *num_chars_opt* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |抽出する文字を含む文字列を指定します。  <br/> |
| _num_chars_opt_ <br/> |省略可能  <br/> |**数値** <br/> |抽出する文字数を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

String
  
## <a name="remarks"></a>Remarks

_Num_chars_opt_の値は、以上のゼロ (0) にする必要があります。 
  
_Num_chars_opt_が文字列の長さよりも大きい場合は、左側がすべてのテキストを返します。 _Num_chars_opt_が省略された場合は 1 であると見なされます。 
  
## <a name="example"></a>例

LEFT ("January 1, 2004", 3) 
  
値 "Jan" を返します。 
  

