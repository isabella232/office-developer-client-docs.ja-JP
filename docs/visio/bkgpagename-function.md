---
title: BKGPAGENAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: 背景ページ名を文字列として返します。
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410316"
---
# <a name="bkgpagename-function"></a>BKGPAGENAME 関数

背景ページ名を文字列として返します。
  
## <a name="syntax"></a>構文

BKGPAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

関数を使用しているページに背景ページがない場合は、"背景 \< \> なし" という文字列が返されます。 
  
無効な言語コードを渡した場合、ローカル言語が使用されます。 
  

