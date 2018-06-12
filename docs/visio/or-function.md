---
title: OR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: パラメーターとして渡された論理式のいずれかが TRUE である場合は、TRUE (1) を返します。
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805948"
---
# <a name="or-function"></a>OR 関数

パラメーターとして渡された論理式のいずれかが TRUE である場合は、TRUE (1) を返します。
  
## <a name="syntax"></a>構文

または (* * *logicalexpression1* * *、* * *logicalexpression2* * *、* * *logicalexpressionN* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |真を評価する最初の式を指定します。  <br/> |
| _logicalexpression2_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |真を評価する 2 番目の式を指定します。  <br/> |
| _logicalexpressionN_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |真を評価する n 番目の式を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

ブール型 (Boolean)
  
## <a name="remarks"></a>注釈

いずれかの式がゼロ以外の値に評価される場合は、TRUE と見なされます。すべての論理式が FALSE または 0 の場合に、この関数は FALSE を返します。 
  
## <a name="example"></a>例

または (高さ\>1 の場合、[pinx] \> 1) 
  
どちらかの式が TRUE の場合、TRUE (1) を返します。両方の式が FALSE の場合にのみ、FALSE (0) を返します。 
  

