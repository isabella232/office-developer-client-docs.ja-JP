---
title: MID 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: 指定した文字の数に基づいて、特定の位置を指定すると、文字列から文字数を返します。
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805903"
---
# <a name="mid-function-visioshapesheet"></a>MID 関数 (VisioShapeSheet)

指定した文字の数に基づいて、特定の位置を指定すると、文字列から文字数を返します。
  
## <a name="syntax"></a>構文

MID (* **テキスト** *、* **開始** *、* **文字数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |抽出する文字を含む文字列を指定します。  <br/> |
| _開始位置_ <br/> |必須  <br/> |**番号** <br/> |抽出する最初の文字の位置を指定します。文字列の最初の文字位置は、1 になります。  <br/> |
| _文字数_ <br/> |必須  <br/> |**番号** <br/> |取り出す文字数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

*開始位置*は、次のとおりです。 場合、 
  
- *テキスト*を返します。 mid 関数の長さより大きい""(空の文字列) です。 
    
- *テキスト*の長さを超える*テキスト*が、*開始位置*と*文字*の長さよりも小さく、*テキスト*の末尾までの文字が返されます。 
    
- start_num が 1 より小さい場合、#VALUE! エラー値を返します。 
    
*文字数*が負の場合は、#VALUE が返されます。 エラー値です。 
  
## <a name="example"></a>例

MID ("SSN 999-99-9999",5,11) 
  
999-99-9999 を返します。 
  

