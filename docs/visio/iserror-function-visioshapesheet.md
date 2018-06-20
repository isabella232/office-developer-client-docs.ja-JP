---
title: ISERROR 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Cellreference の値は、エラーの種類は、かどうかに TRUE を返します。それ以外の場合、FALSE を返します。 ISERROR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805620"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR 関数 (VisioShapeSheet)

_Cellreference_の値は、エラーの種類は、かどうかに TRUE を返します。それ以外の場合、FALSE を返します。 ISERROR 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERROR (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.A1)  <br/> |TRUE  <br/> |
   
ISERROR 関数は #N/A! エラーを認識するため、TRUE を返します。#N/A! エラー以外のすべてのエラー タイプを検出する場合は、ISERR を使用できます。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.X1)  <br/> |TRUE  <br/> |
   
ISERROR 関数は #VALUE! エラーを認識するため、TRUE を返します。#VALUE! エラーを基に式を作成するには、ISERRVALUE 関数を使用します。
  

