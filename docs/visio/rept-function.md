---
title: REPT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
ms.localizationpriority: medium
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: 文字列を指定された回数だけ繰り返して表示します。
ms.openlocfilehash: 4a0741fc5ea15540d61d66d16004e5d0db5e381d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559655"
---
# <a name="rept-function"></a>REPT 関数

文字列を指定された回数だけ繰り返して表示します。 
  
## <a name="syntax"></a>構文

REPT (** *text* **, ** *number_times* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> | 繰り返す文字列を指定します。  <br/> |
| _number_times_ <br/> |必須かどうか  <br/> |**数値** <br/> |文字列の繰り返す回数を、正の数値で指定します。  <br/> |
   
## <a name="remarks"></a>注釈

次  *number_times*  場合: 
  
- number_times がゼロ (0) の場合、"" (空文字列) を返します。
    
- number_times が整数でない場合、小数点以下は切り捨てられます。
    
## <a name="example"></a>例

REPT (" \* ", 5) 
  
を返します \* \* \* \* \* 。 
  

