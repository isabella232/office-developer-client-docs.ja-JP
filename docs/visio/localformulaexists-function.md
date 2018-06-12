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
description: ローカルの数式が参照先のセルに含まれているかどうかを示します。
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805745"
---
# <a name="localformulaexists-function"></a>LOCALFORMULAEXISTS 関数

ローカルの数式が参照先のセルに含まれているかどうかを示します。 
  
## <a name="syntax"></a>構文

LOCALFORMULAEXISTS (* * *cellref* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 数式があるかどうかを調べるセルを指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

ブール型 (Boolean)
  
## <a name="remarks"></a>注釈

LOCALFORMULAEXISTS 関数は、セルがローカルの数式を含む場合は 1 を返し、数式がないか、数式が継承されている場合は 0 (ゼロ) を返します。 
  

