---
title: LOCALFORMULAEXISTS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
ms.localizationpriority: medium
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: 参照先のセルにローカル数式が含まれているかどうかを示します。
ms.openlocfilehash: 2fdd6e547f1f86491fc84d316237d472e767536b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603656"
---
# <a name="localformulaexists-function"></a>LOCALFORMULAEXISTS 関数

参照先のセルにローカル数式が含まれているかどうかを示します。 
  
## <a name="syntax"></a>構文

LOCALFORMULAEXISTS (** *cellref* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |必須  <br/> |**String** <br/> | 数式があるかどうかを調べるセルを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>注釈

LOCALFORMULAEXISTS 関数は、セルがローカルの数式を含む場合は 1 を返し、数式がないか、数式が継承されている場合は 0 (ゼロ) を返します。 
  

