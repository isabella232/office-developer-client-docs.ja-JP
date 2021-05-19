---
title: LOCALFORMULAEXISTS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: 参照先のセルにローカル数式が含まれているかどうかを示します。
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433291"
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
  

