---
title: REPT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: 文字列を指定された回数だけ繰り返して表示します。
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326804"
---
# <a name="rept-function"></a>REPT 関数

文字列を指定された回数だけ繰り返して表示します。 
  
## <a name="syntax"></a>構文

REPT (* * *text* * *、* **繰り返し回数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> | 繰り返す文字列を指定します。  <br/> |
| _繰り返し回数_ <br/> |必須  <br/> |**数値** <br/> |文字列の繰り返す回数を、正の数値で指定します。  <br/> |
   
## <a name="remarks"></a>解説

*繰り返し回数*: 
  
- number_times がゼロ (0) の場合、"" (空文字列) を返します。
    
- number_times が整数でない場合、小数点以下は切り捨てられます。
    
## <a name="example"></a>例

REPT ("\*", 5) 
  
を\* \* \*返し\*ます\*。 
  

