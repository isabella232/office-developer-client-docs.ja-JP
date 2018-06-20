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
description: 背景ページの名前を文字列として返します。
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804905"
---
# <a name="bkgpagename-function"></a>BKGPAGENAME 関数

背景ページの名前を文字列として返します。
  
## <a name="syntax"></a>構文

BKGPAGENAME (* * *langID_opt* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |省略可能  <br/> |**数値** <br/> |関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。  <br/> |
   
### <a name="return-value"></a>�߂�l

String
  
## <a name="remarks"></a>Remarks

関数を使用してページが背景ページでは、文字列を持っていない場合は、"\<背景なし\>"が返されます。 
  
無効な言語コードを渡した場合、ローカル言語が使用されます。 
  

