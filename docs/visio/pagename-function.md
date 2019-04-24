---
title: PAGENAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: ページ名を文字列として返します。
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339467"
---
# <a name="pagename-function"></a>PAGENAME 関数

ページ名を文字列として返します。
  
## <a name="syntax"></a>構文

PAGENAME (* * *langID_opt* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |省略可能  <br/> |**数値** <br/> |関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

無効な言語コードを渡した場合、ローカル言語が使用されます。
  

