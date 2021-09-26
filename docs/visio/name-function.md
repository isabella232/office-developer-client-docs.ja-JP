---
title: NAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
ms.localizationpriority: medium
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: シートの名前を文字列として返します。
ms.openlocfilehash: 7b3bf74d87c534dc99c4ca74d014ded676d0190f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627899"
---
# <a name="name-function"></a>NAME 関数

シートの名前を文字列として返します。
  
## <a name="syntax"></a>構文

NAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |省略可能  <br/> |**数値** <br/> |関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

無効な言語コードを渡した場合、ローカル言語が使用されます。 
  

