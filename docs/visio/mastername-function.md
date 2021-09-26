---
title: MASTERNAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
ms.localizationpriority: medium
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: シートのマスター名を文字列として返します。または、シートにマスターがない場合は文字列 'no master' を返します。
ms.openlocfilehash: 209874e1a1c01c607790f5289ab9d8b183c6fc99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612464"
---
# <a name="mastername-function"></a>MASTERNAME 関数

シートのマスター名を文字列として返します。または、シートにマスター文字が含めなかった場合は文字列 " を \<no master\> 返します。
  
## <a name="syntax"></a>構文

MASTERNAME ([ ** *langID_opt* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |省略可能  <br/> |**数値** <br/> |関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

無効な言語コードを渡した場合、ローカル言語が使用されます。 
  

