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
description: 指定した文字数に基づいて、指定した位置から始まる、テキスト文字列の特定の文字数を返します。
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410267"
---
# <a name="mid-function-visioshapesheet"></a>MID 関数 (VisioShapeSheet)

指定した文字数に基づいて、指定した位置から始まる、テキスト文字列の特定の文字数を返します。
  
## <a name="syntax"></a>構文

MID (** *text* **, ** *start_num* **, **** num_chars ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> |抽出する文字を含む文字列を指定します。  <br/> |
| _start_num_ <br/> |必須  <br/> |**数値** <br/> |抽出する最初の文字の位置を指定します。文字列の最初の文字位置は、1 になります。  <br/> |
| _num_chars_ <br/> |必須  <br/> |**数値** <br/> |取り出す文字数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

次  *start_num*  場合: 
  
- テキストの長さより大  *きい*  場合、MID は "" (空のテキスト) を返します。 
    
- テキストの長さより小さいが *、start_numテキストnum_chars* を超えると、テキストの末尾までの文字が戻 *されます*。 
    
- start_num が 1 より小さい場合、#VALUE! エラー値を返します。 
    
負  *num_chars*  場合、MID は値を返#VALUE! が返されます。 
  
## <a name="example"></a>例

MID ("SSN 999-99-9999",5,11) 
  
999-99-9999 を返します。 
  

