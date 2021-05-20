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
description: 指定した文字数に基づいて、テキスト文字列の一番左の文字または文字を返します。
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427522"
---
# <a name="left-function-visioshapesheet"></a>LEFT 関数 (VisioShapeSheet)

指定した文字数に基づいて、テキスト文字列の一番左の文字または文字を返します。
  
## <a name="syntax"></a>構文

LEFT(** *text* **, [, **** num_chars_opt ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> |抽出する文字を含む文字列を指定します。  <br/> |
| _num_chars_opt_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |抽出する文字数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

値  _は、num_chars_opt_ 0 以上である必要があります。 
  
テキスト  _num_chars_opt_ 長さより大きい場合、LEFT はすべてのテキストを返します。 この  _num_chars_opt_ を省略すると、1 と見なされます。 
  
## <a name="example"></a>例

LEFT ("January 1, 2004", 3) 
  
値 "Jan" を返します。 
  

