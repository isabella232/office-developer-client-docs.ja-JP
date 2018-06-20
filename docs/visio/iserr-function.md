---
title: ISERR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: Cellreference の値が、エラーの種類である場合に TRUE を返します以外の有効です。それ以外の場合、FALSE を返します。 ISERR 関数は、別のセルを参照する数式で使用されます。
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805606"
---
# <a name="iserr-function"></a>ISERR 関数

_Cellreference_の値が、エラーの種類である場合は TRUE を返します以外の有効です。それ以外の場合、FALSE を返します。 ISERR 関数は、別のセルを参照する数式で使用されます。 
  
## <a name="syntax"></a>構文

ISERR (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルの参照を指定します。  <br/> |
   
## <a name="example-1"></a>例 1

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
ISERR 関数は #N/A! エラーを認識しないため、FALSE を返します。すべてのエラー タイプを検出するには、ISERROR を使用します。
  
## <a name="example-2"></a>例 2

|**Cell**|**Formula**|**返される値**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
ISERR 関数は #VALUE! エラーを認識するため、TRUE を返します。
  

