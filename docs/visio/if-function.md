---
title: IF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Logicalexpression が TRUE の場合に、valueiftrue を返します。 Valueiffalse を返します。
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805564"
---
# <a name="if-function"></a>IF 関数

_Logicalexpression_が TRUE の場合に、 _valueiftrue_を返します。 _Valueiffalse_を返します。
  
## <a name="syntax"></a>構文

IF (* * *logicalexpression* * *、* * *valueiftrue* * *、* * *valueiffalse* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |評価する式を指定します。  <br/> |
| _valueiftrue_ <br/> |必須  <br/> |**によって異なります** <br/> |_Logicalexpression_が true のかどうかに返す値です。  <br/> |
| _valueiffalse_ <br/> |必須  <br/> |**によって異なります** <br/> | _Logicalexpression_が false のかどうかに返す値です。  <br/> |
   
### <a name="return-value"></a>�߂�l

可変値
  
## <a name="example"></a>例

IF (高さ\>1.25 で、5、7)
  
図形の高さが 1.25 インチを超える場合は、5 を返します。図形の高さが 1.25 インチ以下の場合は、7 を返します。
  

