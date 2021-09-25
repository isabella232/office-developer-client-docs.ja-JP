---
title: RIGHT 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
ms.localizationpriority: medium
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: 指定した文字数に基づいて、テキスト文字列の最後の文字または文字を返します。
ms.openlocfilehash: 4b4a2cb68f6e15989fade7088e887f852ac4eee8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573517"
---
# <a name="right-function-visioshapesheet"></a>RIGHT 関数 (VisioShapeSheet)

指定した文字数に基づいて、テキスト文字列の最後の文字または文字を返します。
  
## <a name="syntax"></a>構文

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> | 抽出する文字を含む文字列を指定します。  <br/> |
| _num_chars_opt_ <br/> |オプション  <br/> |**数値** <br/> |抽出する文字数を指定します。既定値は 1 です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

値  _は、num_chars_opt_ 0 以上である必要があります。 
  
テキスト  _num_chars_opt_ 長さより大きい場合、RIGHT はすべてのテキストを返します。 この  _num_chars_opt_ を省略すると、1 と見なされます。 
  
## <a name="example"></a>例

RIGHT ("January 1, 2004", 4) 
  
値 2004 を返します。 
  

