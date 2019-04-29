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
description: 指定した文字数に基づいて、指定した位置から開始して、テキスト文字列から特定の数の文字を返します。
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410267"
---
# <a name="mid-function-visioshapesheet"></a>MID 関数 (VisioShapeSheet)

指定した文字数に基づいて、指定した位置から開始して、テキスト文字列から特定の数の文字を返します。
  
## <a name="syntax"></a>構文

MID (* * *text* * *、* **開始位置** *、* ** * 文字数 * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> |抽出する文字を含む文字列を指定します。  <br/> |
| _開始_ <br/> |必須  <br/> |**数値** <br/> |抽出する最初の文字の位置を指定します。 文字列の最初の文字位置は、1 になります。  <br/> |
| _文字数_ <br/> |必須  <br/> |**数値** <br/> |取り出す文字数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

*開始位置*は次のようになります。 
  
- *文字列*の長さより大きい場合、MID は "" (空の文字列) を返します。 
    
- *文字列*の長さを超えていますが、 ** *開始位置*と文字数が*文字列*の長さを超えている場合、MID は*文字列*の末尾までの文字数を返します。 
    
- start_num が 1 より小さい場合、#VALUE! エラー値を返します。 
    
文字** 数が負の数である場合、MID は #VALUE を返します。 が返されます。 
  
## <a name="example"></a>例

MID ("SSN 999-99-9999",5,11) 
  
999-99-9999 を返します。 
  

