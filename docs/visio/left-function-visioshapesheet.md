---
title: LEFT 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
ms.localizationpriority: medium
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: 指定した文字数に基づいて、テキスト文字列の一番左の文字または文字を返します。
ms.openlocfilehash: 31b690c231f59bed53b8d04b0a4298621a718101
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554510"
---
# <a name="left-function-visioshapesheet"></a>LEFT 関数 (VisioShapeSheet)

指定した文字数に基づいて、テキスト文字列の一番左の文字または文字を返します。
  
## <a name="syntax"></a>構文

LEFT(** *text* **, [, **** num_chars_opt ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> |抽出する文字を含む文字列を指定します。  <br/> |
| _num_chars_opt_ <br/> |オプション  <br/> |**数値型 (Numeric)** <br/> |抽出する文字数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

値  _は、num_chars_opt_ 0 以上である必要があります。 
  
テキスト  _num_chars_opt_ 長さより大きい場合、LEFT はすべてのテキストを返します。 この  _num_chars_opt_ を省略すると、1 と見なされます。 
  
## <a name="example"></a>例

LEFT ("January 1, 2004", 3) 
  
値 "Jan" を返します。 
  

